---
description: Como depurar o Microsoft Edge (Chromium) e o Microsoft Edge (EdgeHTML) Visual Studio Code
title: Depurar o Microsoft Edge (Chromium) do Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desenvolvimento da Web, ferramentas f12, devtools, vs code, código do visual studio, depurador
ms.openlocfilehash: e36348fc1ef5e30a511e6eda73c7646a85d8717e
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399292"
---
# <a name="debugger-for-microsoft-edge-visual-studio-code-extension"></a><span data-ttu-id="c0f47-104">Depurador para o Microsoft Edge Visual Studio Extensão de Código</span><span class="sxs-lookup"><span data-stu-id="c0f47-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="c0f47-105">Com a [extensão Depurador][VisualstudioMarketplaceDebuggerMicrosoftEdge] do Microsoft Edge Visual Studio Code, depure sua linha de código JavaScript front-end por linha e consulte instruções diretamente de `console.log()` Visual Studio [Code][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="c0f47-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para borda Visual Studio de código no trabalho" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="c0f47-107">Depurador para borda Visual Studio de código no trabalho</span><span class="sxs-lookup"><span data-stu-id="c0f47-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <a name="launching-microsoft-edge"></a><span data-ttu-id="c0f47-108">Iniciando o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0f47-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="c0f47-109">Navegue até o exibição de depuração \( `Ctrl` + `Shift` + `D` no Windows ou `Command` + `Shift` + `D` no macOS\) na Barra **de Atividades.**</span><span class="sxs-lookup"><span data-stu-id="c0f47-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="c0f47-110">Se você não tiver nenhuma configuração no código Visual Studio, selecione no Windows ou macOS ou `F5` selecione o botão verde **Reproduzir.**</span><span class="sxs-lookup"><span data-stu-id="c0f47-110">If you do not have any configurations in Visual Studio Code, select `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="c0f47-111">Selecione **Borda** no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="c0f47-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="c0f47-112">Você deve ver um `launch.json` arquivo com a configuração a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0f47-112">You should see a `launch.json` file with the following configuration.</span></span>  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```  

<span data-ttu-id="c0f47-113">Se você selecionar no Windows ou macOS ou selecionar o botão verde Reproduzir novamente, Visual Studio Code iniciará o `F5` Microsoft Edge \(EdgeHTML\) e poderá depurar qualquer projeto da Web executado na porta diretamente de Visual Studio \*\*\*\* `8080` Code!</span><span class="sxs-lookup"><span data-stu-id="c0f47-113">If you select `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <a name="microsoft-edge-chromium"></a><span data-ttu-id="c0f47-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="c0f47-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="c0f47-115">Se você quiser iniciar o Microsoft Edge \(Chromium\), o novo Microsoft Edge, em vez do Microsoft Edge \(EdgeHTML\), basta adicionar um atributo à configuração existente com a versão do `version` Microsoft Edge \(Chromium\) que deseja iniciar \( `dev` , ou `beta` `canary` \).</span><span class="sxs-lookup"><span data-stu-id="c0f47-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="c0f47-116">A configuração a seguir inicia a versão canária do Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="c0f47-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="c0f47-117">Anexando ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0f47-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="c0f47-118">Anexar Visual Studio código ao Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="c0f47-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="c0f47-119">No terminal, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="c0f47-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="c0f47-120">Adicione a configuração abaixo ao seu `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="c0f47-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="c0f47-121">Se você executar essa configuração agora, Visual Studio Code anexa ao Microsoft Edge \(Chromium\) e inicie a depuração.</span><span class="sxs-lookup"><span data-stu-id="c0f47-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <a name="getting-in-touch-with-the-elements-for-microsoft-edge-visual-studio-code-extension-team"></a><span data-ttu-id="c0f47-122">Entrar em contato com a equipe de extensão Elements for Microsoft Edge Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c0f47-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="c0f47-123">Envie seus comentários [arquivando um problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] no [repositório do GitHub][GithubMicrosoftVscodeEdgeDebug2] da extensão.</span><span class="sxs-lookup"><span data-stu-id="c0f47-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="c0f47-124">Inclua o arquivo de log do adaptador de depuração, que é criado para cada executar no `%temp%` diretório com o nome `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="c0f47-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="c0f47-125">Arraste esse arquivo para um comentário de problema para enviá-lo para o GitHub.</span><span class="sxs-lookup"><span data-stu-id="c0f47-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="c0f47-126">Para ajudar a melhorar a extensão de Código de Elementos do Microsoft Edge Visual Studio, suas contribuições são bem-vindas!</span><span class="sxs-lookup"><span data-stu-id="c0f47-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="c0f47-127">Encontre tudo o que você precisa para começar no [repositório gitHub][GithubMicrosoftVscodeEdgeDebug2] da extensão.</span><span class="sxs-lookup"><span data-stu-id="c0f47-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]: ./media/debugger-for-edge.png "Depurador para borda Visual Studio extensão de código em ação"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Código"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Visual Studio Código"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "microsoft/vscode-edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Novo problema - microsoft/vscode-edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para o Microsoft Edge | Visual Studio Marketplace"  
