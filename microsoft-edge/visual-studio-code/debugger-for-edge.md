---
description: Como depurar o Microsoft Edge (Chromium) e o Microsoft Edge (EdgeHTML) a partir de código VS
title: Depurar o Microsoft Edge (Chromium) a partir de código VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, depurador
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562469"
---
# <span data-ttu-id="16294-104">Depurador para extensão de código do Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="16294-104">Debugger for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="16294-105">Com o [depurador para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código, você pode depurar o código JavaScript front-end linha por linha e ver `console.log()` instruções diretamente do [código do Visual Studio](https://code.visualstudio.com/)!</span><span class="sxs-lookup"><span data-stu-id="16294-105">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug your front-end JavaScript code line by line and see `console.log()` statements all directly from [Visual Studio Code](https://code.visualstudio.com/)!</span></span>

![GIF do depurador para Edge VS extensão de código no trabalho](./media/debugger-for-edge.gif)

## <span data-ttu-id="16294-107">Iniciando o Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="16294-107">Launching Microsoft Edge</span></span>

<span data-ttu-id="16294-108">Navegue até o modo de exibição de depuração ( `Ctrl`  +  `Shift`  +  `D` no Windows ou `Command`  +  `Shift`  +  `D` no Mac) na **barra de atividades**.</span><span class="sxs-lookup"><span data-stu-id="16294-108">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac) in the **Activity Bar**.</span></span> <span data-ttu-id="16294-109">Se você não tiver nenhuma configuração no código do VS, pressione `F5` no Windows ou Mac ou clique no botão de **reprodução** verde.</span><span class="sxs-lookup"><span data-stu-id="16294-109">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="16294-110">Selecione "borda" na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="16294-110">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="16294-111">Agora, você verá um arquivo **inicialização. JSON** com a seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="16294-111">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="16294-112">Se você agora pressionar `F5` no Windows ou Mac ou clicar no botão verde de **reprodução** novamente, o código do vs iniciará o Microsoft Edge (EdgeHTML) e você poderá depurar qualquer projeto Web que você esteja executando na porta **8080** diretamente de um código vs!</span><span class="sxs-lookup"><span data-stu-id="16294-112">If you now press `F5` on Windows or Mac or click the green **Play** button again, VS Code will launch Microsoft Edge (EdgeHTML) and you will be able to debug any web project you have running on port **8080** directly from VS Code!</span></span>

### <span data-ttu-id="16294-113">Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="16294-113">Microsoft Edge (Chromium)</span></span>

<span data-ttu-id="16294-114">Se você quiser iniciar o Microsoft Edge (Chromium), a próxima versão do Microsoft Edge, em vez do Microsoft Edge (EdgeHTML), basta adicionar um `version` atributo à sua configuração existente com a versão do Microsoft Edge (Chromium) que você deseja iniciar ( `dev` , `beta` ou ou `canary` ).</span><span class="sxs-lookup"><span data-stu-id="16294-114">If you want to launch Microsoft Edge (Chromium), the next version of Microsoft Edge, instead of Microsoft Edge (EdgeHTML), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="16294-115">A configuração a seguir inicializará a versão Canárias do Microsoft Edge (Chromium):</span><span class="sxs-lookup"><span data-stu-id="16294-115">The configuration below will launch the Canary version of Microsoft Edge (Chromium):</span></span>

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

## <span data-ttu-id="16294-116">Anexando ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="16294-116">Attaching to Microsoft Edge</span></span>

<span data-ttu-id="16294-117">Você também pode anexar o código VS ao Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="16294-117">You can also attach VS Code to Microsoft Edge (Chromium).</span></span> <span data-ttu-id="16294-118">Em seu terminal, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="16294-118">From your terminal, run the following command:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="16294-119">Adicione a configuração abaixo ao arquivo **. JSON de inicialização** :</span><span class="sxs-lookup"><span data-stu-id="16294-119">Add the configuration below to your **launch.json** file:</span></span>

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

<span data-ttu-id="16294-120">Se agora você executar essa configuração, o código do VS será anexado ao Microsoft Edge (Chromium) e você poderá iniciar a depuração!</span><span class="sxs-lookup"><span data-stu-id="16294-120">If you now run this configuration, VS Code will attach to Microsoft Edge (Chromium) and you can start debugging!</span></span>

## <span data-ttu-id="16294-121">Privacidade Jurídica</span><span class="sxs-lookup"><span data-stu-id="16294-121">Feedback</span></span>

<span data-ttu-id="16294-122">Envie-nos seus comentários [arquivando um problema](https://github.com/Microsoft/vscode-edge-debug2/issues/new) em relação ao [repositório GitHub](https://github.com/Microsoft/vscode-edge-debug2)da extensão.</span><span class="sxs-lookup"><span data-stu-id="16294-122">Send us your feedback by [filing an issue](https://github.com/Microsoft/vscode-edge-debug2/issues/new) against this extension's [GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span> <span data-ttu-id="16294-123">Inclua o arquivo de log do adaptador de depuração, que é criado para cada execução no diretório% Temp% com o nome `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="16294-123">Please include the debug adapter log file, which is created for each run in the %temp% directory with the name `vscode-edge-debug2.txt`.</span></span> <span data-ttu-id="16294-124">Você pode arrastar esse arquivo para um comentário de questão para carregá-lo no GitHub.</span><span class="sxs-lookup"><span data-stu-id="16294-124">You can drag this file into an issue comment to upload it to GitHub.</span></span>

<span data-ttu-id="16294-125">Se você quiser nos ajudar a aprimorar essa extensão, Agradecemos suas contribuições!</span><span class="sxs-lookup"><span data-stu-id="16294-125">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="16294-126">Você pode encontrar tudo o que precisa para começar a usar o [repositório do GitHub](https://github.com/Microsoft/vscode-edge-debug2).</span><span class="sxs-lookup"><span data-stu-id="16294-126">You can find everything you need to get started in [our GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span>