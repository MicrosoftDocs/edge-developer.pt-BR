---
description: Como depurar o Microsoft Edge (Chromium) e o Microsoft Edge (EdgeHTML) a partir do código do Visual Studio
title: Depurar o Microsoft Edge (Chromium) a partir do código do Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador
ms.openlocfilehash: df15b76cc26ad01d3b8508362aa4b86998f8b41b
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182502"
---
# <span data-ttu-id="acb29-104">Depurador para extensão de código do Microsoft Edge Visual Studio</span><span class="sxs-lookup"><span data-stu-id="acb29-104">Debugger For Microsoft Edge Visual Studio Code Extension</span></span>  

<span data-ttu-id="acb29-105">Com o [depurador para extensão de código do Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio, depure o código JavaScript front-end linha por linha e veja `console.log()` instruções diretamente do [código do Visual Studio][VisualstudioCode]!</span><span class="sxs-lookup"><span data-stu-id="acb29-105">With the [Debugger for Microsoft Edge][VisualstudioMarketplaceDebuggerMicrosoftEdge] Visual Studio Code extension, debug your front-end JavaScript code line by line and see `console.log()` statements directly from [Visual Studio Code][VisualstudioCode]!</span></span>  

:::image type="complex" source="./media/debugger-for-edge.gif" alt-text="Depurador para extensão de código do Edge Visual Studio no trabalho" lightbox="./media/debugger-for-edge.gif":::
   <span data-ttu-id="acb29-107">Depurador para extensão de código do Edge Visual Studio no trabalho</span><span class="sxs-lookup"><span data-stu-id="acb29-107">Debugger for Edge Visual Studio Code extension at work</span></span>  
:::image-end:::

<!--![Debugger for Edge Visual Studio Code extension at work][ImageGifDebuggerEdge]  -->  

## <span data-ttu-id="acb29-108">Iniciando o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="acb29-108">Launching Microsoft Edge</span></span>  

<span data-ttu-id="acb29-109">Navegue até o modo de exibição de depuração \ ( `Ctrl` + `Shift` + `D` no Windows ou `Command` + `Shift` + `D` no MacOS \) na **barra de atividades**.</span><span class="sxs-lookup"><span data-stu-id="acb29-109">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\) in the **Activity Bar**.</span></span>  <span data-ttu-id="acb29-110">Se você não tiver nenhuma configuração no código do Visual Studio, pressione `F5` no Windows ou no MacOS ou selecione o botão de **reprodução** verde.</span><span class="sxs-lookup"><span data-stu-id="acb29-110">If you do not have any configurations in Visual Studio Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="acb29-111">Selecione **borda** na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="acb29-111">Select **Edge** in the dropdown.</span></span>  <span data-ttu-id="acb29-112">Você deve ver um `launch.json` arquivo com a configuração a seguir.</span><span class="sxs-lookup"><span data-stu-id="acb29-112">You should see a `launch.json` file with the following configuration.</span></span>  

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

<span data-ttu-id="acb29-113">Se você pressionar `F5` o Windows ou o MacOS ou selecionar o botão de **reprodução** verde novamente, o código do Visual Studio inicializará o Microsoft Edge \ (EdgeHTML \) e você poderá depurar qualquer projeto da Web que esteja executando na porta `8080` diretamente do código do Visual Studio!</span><span class="sxs-lookup"><span data-stu-id="acb29-113">If you press `F5` on Windows or macOS or select the green **Play** button again, Visual Studio Code launches Microsoft Edge \(EdgeHTML\) and you are able to debug any web project you have running on port `8080` directly from Visual Studio Code!</span></span>  

### <span data-ttu-id="acb29-114">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="acb29-114">Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="acb29-115">Se você quiser iniciar o Microsoft Edge \ (Chromium \), o novo Microsoft Edge, em vez do Microsoft Edge \ (EdgeHTML \), basta adicionar um `version` atributo à sua configuração existente com a versão do Microsoft Edge \ (Chromium \) que você deseja iniciar \ ( `dev` , `beta` ou `canary` \).</span><span class="sxs-lookup"><span data-stu-id="acb29-115">If you want to launch Microsoft Edge \(Chromium\), the new Microsoft Edge, instead of Microsoft Edge \(EdgeHTML\), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge \(Chromium\) you want to launch \(`dev`, `beta`, or `canary`\).</span></span>  <span data-ttu-id="acb29-116">A seguinte configuração a seguir inicia a versão Canárias do Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="acb29-116">The following configuration below launches the Canary version of Microsoft Edge \(Chromium\).</span></span>  

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

## <span data-ttu-id="acb29-117">Anexando ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="acb29-117">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="acb29-118">Anexe o código do Visual Studio ao Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="acb29-118">Attach Visual Studio Code to Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="acb29-119">Em seu terminal, execute o seguinte comando.</span><span class="sxs-lookup"><span data-stu-id="acb29-119">From your terminal, run the following command.</span></span>  

```shell
start msedge --remote-debugging-port=9222
```  

<span data-ttu-id="acb29-120">Adicione a configuração abaixo ao seu `launch.json` arquivo.</span><span class="sxs-lookup"><span data-stu-id="acb29-120">Add the configuration below to your `launch.json` file.</span></span>   

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```  

<span data-ttu-id="acb29-121">Se agora você executar essa configuração, o código do Visual Studio será anexado ao Microsoft Edge \ (Chromium \) e iniciará a depuração.</span><span class="sxs-lookup"><span data-stu-id="acb29-121">If you now run this configuration, Visual Studio Code attaches to Microsoft Edge \(Chromium\) and start debugging.</span></span>  

## <span data-ttu-id="acb29-122">Entrar em contato com os elementos da equipe de extensão de código do Visual Studio do Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="acb29-122">Getting in touch with the Elements for Microsoft Edge Visual Studio Code extension team</span></span>    

<span data-ttu-id="acb29-123">Envie seus comentários por meio do [arquivamento de um problema][GithubMicrosoftVscodeEdgeDebug2NewIssue] no [repositório do GitHub][GithubMicrosoftVscodeEdgeDebug2] da extensão.</span><span class="sxs-lookup"><span data-stu-id="acb29-123">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDebug2NewIssue] against in the [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  <span data-ttu-id="acb29-124">Inclua o arquivo de log do adaptador de depuração, que é criado para cada execução no `%temp%` diretório com o nome `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="acb29-124">Please include the debug adapter log file, which is created for each run in the `%temp%` directory with the name `vscode-edge-debug2.txt`.</span></span>  <span data-ttu-id="acb29-125">Arraste este arquivo para um comentário de problema para carregá-lo no GitHub.</span><span class="sxs-lookup"><span data-stu-id="acb29-125">Drag this file into an issue comment to upload it to GitHub.</span></span>  

<span data-ttu-id="acb29-126">Para ajudar a melhorar a extensão de código do Microsoft Edge Visual Studio, suas contribuições são bem-vindas!</span><span class="sxs-lookup"><span data-stu-id="acb29-126">To help make the Elements for Microsoft Edge Visual Studio Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="acb29-127">Encontre tudo o que você precisa para começar a usar o [repositório do GitHub][GithubMicrosoftVscodeEdgeDebug2] da extensão.</span><span class="sxs-lookup"><span data-stu-id="acb29-127">Find everything you need to get started in [GitHub repo][GithubMicrosoftVscodeEdgeDebug2] of the extension.</span></span>  


<!-- image links -->  

<!--[ImageGifDebuggerEdge]: ./media/debugger-for-edge.gif "Debugger for Edge Visual Studio Code extension in action"  -->  
[ImagePngDebuggerEdge]:./Media/debugger-for-edge.png "depurador para Edge extensão de código do Visual Studio em ação"  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Código do Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentação | Código do Visual Studio"   

[GithubMicrosoftVscodeEdgeDebug2]: https://github.com/Microsoft/vscode-edge-debug2 "Microsoft/vscode-Edge-debug2 | GitHub"  
[GithubMicrosoftVscodeEdgeDebug2NewIssue]: https://github.com/Microsoft/vscode-edge-debug2/issues/new "Novo problema-Microsoft/vscode-Edge-debug2 | GitHub"  

[VisualstudioMarketplaceDebuggerMicrosoftEdge]: https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge "Depurador para Microsoft Edge | Visual Studio Marketplace"  
