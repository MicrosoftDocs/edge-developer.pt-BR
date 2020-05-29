---
description: Como usar os elementos do Microsoft Edge (Chromium) a partir do código VS
title: Elementos do Microsoft Edge (Chromium) de código VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desenvolvimento da Web, Ferramentas F12, devtools, código vs, código do Visual Studio, elementos
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562473"
---
# <span data-ttu-id="7cb5b-104">Elementos da extensão de código do Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="7cb5b-104">Elements for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="7cb5b-105">Ao adicionar os [elementos para Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) vs extensão de código, você pode usar a ferramenta elementos do navegador dentro do [código do Visual Studio](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="7cb5b-105">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within [Visual Studio Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="7cb5b-106">Ao iniciar ou anexar, a ferramenta elementos será conectada a uma instância do Microsoft Edge, exibirá a estrutura HTML do tempo de execução e permitirá que você altere o layout ou corrija os problemas de estilo.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-106">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

![GIF dos elementos para Edge VS extensão de código no trabalho](./media/elements-for-edge.gif)

## <span data-ttu-id="7cb5b-108">Iniciando o Microsoft Edge da extensão de elementos</span><span class="sxs-lookup"><span data-stu-id="7cb5b-108">Launching Microsoft Edge From the Elements extension</span></span> 

<span data-ttu-id="7cb5b-109">Navegue até elementos na **barra de atividades**.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-109">Navigate to Elements in the **Activity Bar**.</span></span> <span data-ttu-id="7cb5b-110">Ao lado do local em que diz "elementos para Microsoft Edge: targets", há um sinal de adição que abrirá o navegador do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-110">Next to where it says "Elements for Microsoft Edge: Targets," there is a plus sign that will open the browser for your app.</span></span> <span data-ttu-id="7cb5b-111">Se você tiver selecionado a opção *about: Blank* , será preciso navegar até seu aplicativo Web no navegador para que ele seja exibido no painel de elementos em vs Code.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-111">If you selected the *about:blank* option, you will have to navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>

## <span data-ttu-id="7cb5b-112">Iniciando o Microsoft Edge a partir do modo de exibição de depuração</span><span class="sxs-lookup"><span data-stu-id="7cb5b-112">Launching Microsoft Edge from the Debug view</span></span>

<span data-ttu-id="7cb5b-113">Se você estiver acostumado a usar o modo de exibição de depuração no código do Visual Studio, poderá acessar os elementos dessa ferramenta.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-113">If you are accustomed to using the Debug view in Visual Studio Code, you can access Elements from that tool.</span></span> <span data-ttu-id="7cb5b-114">Navegue até o modo de exibição de depuração ( `Ctrl`  +  `Shift`  +  `D` no Windows ou `Command`  +  `Shift`  +  `D` no Mac).</span><span class="sxs-lookup"><span data-stu-id="7cb5b-114">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac).</span></span> 

<span data-ttu-id="7cb5b-115">Se você não tiver nenhuma configuração no código do VS, pressione `F5` no Windows ou Mac ou clique no botão de **reprodução** verde.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-115">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="7cb5b-116">Selecione "borda" na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-116">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="7cb5b-117">Agora, você verá um arquivo **inicialização. JSON** com a seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="7cb5b-117">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="7cb5b-118">Agora que você carregou a configuração correta, pressione `F5` no Windows ou no Mac ou clique no botão verde **Play** .</span><span class="sxs-lookup"><span data-stu-id="7cb5b-118">Now that you have loaded the correct configuration, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="7cb5b-119">A ferramenta de elementos com a qual você está familiarizado com o navegador Microsoft Edge agora será iniciada no código VS, permitindo que você acesse o screencast do seu navegador e examine os componentes da página.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-119">The Elements tool you are familiar with from the Microsoft Edge browser will now launch in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>

## <span data-ttu-id="7cb5b-120">Anexando ao Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7cb5b-120">Attaching to Microsoft Edge</span></span>
<span data-ttu-id="7cb5b-121">Se quiser anexar o código VS a uma instância do Microsoft Edge (Chromium), você deve iniciar o navegador executando o seguinte comando em seu teminal:</span><span class="sxs-lookup"><span data-stu-id="7cb5b-121">If you'd like to attach VS Code to an instance of Microsoft Edge (Chromium), you must start the browser by running the following command from your teminal:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="7cb5b-122">Depois que o aplicativo for iniciado, adicione a configuração abaixo ao arquivo **. JSON de inicialização** :</span><span class="sxs-lookup"><span data-stu-id="7cb5b-122">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>

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

<span data-ttu-id="7cb5b-123">Selecione "anexar ao Microsoft Edge e abra a ferramenta elementos" no menu suspenso depurador.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-123">Select "Attach to Microsoft Edge and open the Elements tool" from the Debugger drop-down menu.</span></span> <span data-ttu-id="7cb5b-124">Em seguida, pressione `F5` no Windows ou Mac ou clique no botão de **reprodução** verde.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-124">Next, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="7cb5b-125">O código VS iniciará a ferramenta elementos, permitindo que você acesse o screencast do seu navegador, inspecione o DOM e o estilo dos componentes na página.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-125">VS Code will launch the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>

## <span data-ttu-id="7cb5b-126">Privacidade Jurídica</span><span class="sxs-lookup"><span data-stu-id="7cb5b-126">Feedback</span></span>
<span data-ttu-id="7cb5b-127">Envie-nos seus comentários [arquivando um problema](https://github.com/microsoft/vscode-edge-devtools/issues/new) em relação ao [repositório GitHub](https://github.com/microsoft/vscode-edge-devtools)da extensão.</span><span class="sxs-lookup"><span data-stu-id="7cb5b-127">Send us your feedback by [filing an issue](https://github.com/microsoft/vscode-edge-devtools/issues/new) against this extension's [GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span> 

<span data-ttu-id="7cb5b-128">Se você quiser nos ajudar a aprimorar essa extensão, Agradecemos suas contribuições!</span><span class="sxs-lookup"><span data-stu-id="7cb5b-128">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="7cb5b-129">Você pode encontrar tudo o que precisa para começar a usar o [repositório do GitHub](https://github.com/microsoft/vscode-edge-devtools).</span><span class="sxs-lookup"><span data-stu-id="7cb5b-129">You can find everything you need to get started in [our GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span>