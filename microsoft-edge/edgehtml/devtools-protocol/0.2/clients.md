---
description: O protocolo Microsoft Edge DevTools versão 0,2 dá suporte aos seguintes clientes de ferramentas.
title: Microsoft Edge DevTools Protocol versão 0,2 clientes (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b471ff5a4051411fc205a269d811524c38acac72
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231311"
---
# <span data-ttu-id="4d85c-103">Microsoft Edge DevTools Protocol versão 0,2 clientes (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="4d85c-103">Microsoft Edge DevTools Protocol Version 0.2 Clients (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="4d85c-104">A versão 0,2 do protocolo Microsoft Edge DevTools funciona apenas na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="4d85c-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>  

<span data-ttu-id="4d85c-105">O **protocolo DevTools 0,2** dá suporte aos seguintes clientes de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="4d85c-105">**DevTools Protocol 0.2** supports the following tooling clients.</span></span>

<span data-ttu-id="4d85c-106">[ ![ Código do Visual Studio](../media/visual-studio-code.png)](#visual-studio-code) Microsoft [ ![ Edge devtools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ do Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span><span class="sxs-lookup"><span data-stu-id="4d85c-106">[![Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [![Visual Studio Code](../media/visual-studio-code.png)](#visual-studio-code) [![Microsoft Visual Studio 15.8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span></span>

## <span data-ttu-id="4d85c-107">Visualização do Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4d85c-107">Microsoft Edge DevTools Preview</span></span>

<span data-ttu-id="4d85c-108">Você pode usar o aplicativo autônomo do [**Microsoft Edge devtools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) para Windows 10 da Microsoft Store para depurar remotamente um dispositivo host executando o Microsoft Edge ([EdgeHTML 17](../../dev-guide/index.md) ou posterior).</span><span class="sxs-lookup"><span data-stu-id="4d85c-108">You can use the standalone [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 app from the Microsoft Store to remotely debug a host device running Microsoft Edge ([EdgeHTML 17](../../dev-guide/index.md) or later).</span></span>

<span data-ttu-id="4d85c-109">A versão 0,2 do protocolo DevTools fornece novos domínios para a depuração de estilo e de layout e APIs de console, além da funcionalidade de depuração de script principal introduzida na versão 0,1.</span><span class="sxs-lookup"><span data-stu-id="4d85c-109">Version 0.2 of the DevTools Protocol provides new domains for style and layout debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="4d85c-110">Na interface do usuário de borda DevTools, isso se traduz em funcionalidades disponíveis nos painéis de [**elementos**](../../devtools-guide/elements.md), [**console**](../../devtools-guide/console.md) e [**depurador**](../../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="4d85c-110">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md) panels.</span></span> <span data-ttu-id="4d85c-111">Atualmente a depuração remota do Microsoft Edge está limitada aos hosts da área de trabalho, com suporte a outros dispositivos Windows 10 em lançamentos futuros.</span><span class="sxs-lookup"><span data-stu-id="4d85c-111">Currently Microsoft Edge remote debugging is limited to desktop hosts, with support for other Windows 10 devices coming in future releases.</span></span>

<span data-ttu-id="4d85c-112">Confira aqui como configurar a depuração remota com o aplicativo Microsoft Edge DevTools Preview.</span><span class="sxs-lookup"><span data-stu-id="4d85c-112">Here's how to set up remote debugging with the Microsoft Edge DevTools Preview app.</span></span> <span data-ttu-id="4d85c-113">A 0,2 versão do protocolo DevTools requer a [atualização do Windows 10 de outubro de 2018](/windows/uwp/whats-new/windows-10-build-17763) ou uma compilação mais recente do Windows Insider Preview na máquina do host (depurador).</span><span class="sxs-lookup"><span data-stu-id="4d85c-113">The DevTools Protocol version 0.2 requires [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later Windows Insider Preview build on the host (debugee) machine.</span></span> <span data-ttu-id="4d85c-114">O aplicativo Edge DevTools Preview (usado na máquina do depurador) será executado no Windows 10 versão 16299 (atualização do Windows 10 para criadores de outono, 10/2017) ou superior.</span><span class="sxs-lookup"><span data-stu-id="4d85c-114">The Edge DevTools Preview app (used on the debugger machine) will run on Windows 10 version 16299 (Windows 10 Fall Creators Update, 10/2017) or higher.</span></span>

**<span data-ttu-id="4d85c-115">Na máquina do host (depurador)...</span><span class="sxs-lookup"><span data-stu-id="4d85c-115">On the host (debugee) machine...</span></span>**

1. <span data-ttu-id="4d85c-116">Se você estiver em uma rede WiFi, verifique se a rede está marcada como **Domain** ou **Private**.</span><span class="sxs-lookup"><span data-stu-id="4d85c-116">If you're on a WiFi network, ensure the network is marked as either **Domain** or **Private**.</span></span> <span data-ttu-id="4d85c-117">Você pode verificar isso abrindo o aplicativo da [**central de segurança do Windows Defender**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , clicando em **Firewall & proteção de rede** e verificando se sua rede está listada como uma rede *privada*ou de *domínio* .</span><span class="sxs-lookup"><span data-stu-id="4d85c-117">You can verify this by opening the [**Windows Defender Security Center**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) app, clicking on **Firewall & network protection** and checking if your network is listed as a *Domain network* or *Private network*.</span></span> 

    <span data-ttu-id="4d85c-118">Se ele estiver listado como *público*, acesse **configurações**  >  **rede & Internet**  >  **Wi-Fi**, clique em sua rede e alterne o botão do *perfil de rede* para **particular**.</span><span class="sxs-lookup"><span data-stu-id="4d85c-118">If its listed as *Public*, go to **Settings** > **Network & Internet** > **Wi-Fi**, click on your network and toggle the *Network profile* button to **Private**.</span></span>

2. <span data-ttu-id="4d85c-119">Abra o painel **de controle para desenvolvedores** nas *configurações* do Windows (procure *desenvolvedor* e clique em *usar recursos de desenvolvedor*) e:</span><span class="sxs-lookup"><span data-stu-id="4d85c-119">Open the **For developers** control panel in Windows *Settings* (search for *developer* and click on *Use developer features*), and:</span></span> 

    <span data-ttu-id="4d85c-120">a.</span><span class="sxs-lookup"><span data-stu-id="4d85c-120">a.</span></span> <span data-ttu-id="4d85c-121">Ative o **modo de desenvolvedor**.</span><span class="sxs-lookup"><span data-stu-id="4d85c-121">Toggle on **Developer Mode**.</span></span> <span data-ttu-id="4d85c-122">Isso vai instalar o pacote do *modo de desenvolvedor* , permitindo ferramentas remotas para área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d85c-122">This will install the *Developer Mode* package, enabling remote tooling for desktop.</span></span>

    <span data-ttu-id="4d85c-123">b.</span><span class="sxs-lookup"><span data-stu-id="4d85c-123">b.</span></span> <span data-ttu-id="4d85c-124">Habilite o Device [**portal**](/windows/uwp/debug-test-perf/device-portal) (*ative o diagnóstico remoto em conexões de rede local*) e a **descoberta de dispositivo** (*torne seu dispositivo visível para conexões USB e sua rede local*).</span><span class="sxs-lookup"><span data-stu-id="4d85c-124">Enable [**Device Portal**](/windows/uwp/debug-test-perf/device-portal) (*Turn on remote diagnostics over local area network connections*) and **Device discovery** (*Make your device visible to USB connections and your local network*).</span></span>

    <span data-ttu-id="4d85c-125">c.</span><span class="sxs-lookup"><span data-stu-id="4d85c-125">c.</span></span> <span data-ttu-id="4d85c-126">Ative a **autenticação** e forneça um nome de usuário/senha.</span><span class="sxs-lookup"><span data-stu-id="4d85c-126">Turn on **Authentication** and supply a username / password.</span></span>

    <span data-ttu-id="4d85c-127">d.</span><span class="sxs-lookup"><span data-stu-id="4d85c-127">d.</span></span> <span data-ttu-id="4d85c-128">Observação: o endereço IP do computador e a porta de conexão (50443) são exibidos.</span><span class="sxs-lookup"><span data-stu-id="4d85c-128">Note the machine IP address and connection port (50443) displayed.</span></span>

3. <span data-ttu-id="4d85c-129">Abra as guias no Microsoft Edge que você deseja depurar do computador cliente.</span><span class="sxs-lookup"><span data-stu-id="4d85c-129">Open tabs in Microsoft Edge that you wish to debug from the client machine.</span></span>

**<span data-ttu-id="4d85c-130">Na máquina cliente (depurador)...</span><span class="sxs-lookup"><span data-stu-id="4d85c-130">On the client (debugger) machine...</span></span>**

1.  <span data-ttu-id="4d85c-131">Instale e inicie o aplicativo autônomo de [visualização do Microsoft Edge devtools](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) na Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="4d85c-131">Install and launch the standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app from the Microsoft Store.</span></span>

2. <span data-ttu-id="4d85c-132">Abra o painel **remoto** e insira o local de rede (URL e porta) do computador host e clique em **conectar**.</span><span class="sxs-lookup"><span data-stu-id="4d85c-132">Open the **Remote** panel and enter the network location (URL and port) of the host machine and click **Connect**.</span></span>

3. <span data-ttu-id="4d85c-133">**Instale** o certificado do computador host a partir da caixa de diálogo *certificado não confiável* exibida.</span><span class="sxs-lookup"><span data-stu-id="4d85c-133">**Install** the host machine's certificate from the *Untrusted Certificate* dialog that appears.</span></span>

4. <span data-ttu-id="4d85c-134">Forneça o nome de usuário/senha designado para a autenticação do Device Portal.</span><span class="sxs-lookup"><span data-stu-id="4d85c-134">Supply the username/password you designated for Device Portal authentication.</span></span>

5. <span data-ttu-id="4d85c-135">O painel *remoto* carregará uma lista de destinos de página do debuggable no computador host.</span><span class="sxs-lookup"><span data-stu-id="4d85c-135">The *Remote* panel will load a list of debuggable page targets on the host machine.</span></span> <span data-ttu-id="4d85c-136">Selecione um para iniciar a depuração.</span><span class="sxs-lookup"><span data-stu-id="4d85c-136">Select one to start debugging.</span></span>

6. <span data-ttu-id="4d85c-137">Use o botão **Atualizar** para atualizar e recarregar a lista de destinos de página remotas no computador host.</span><span class="sxs-lookup"><span data-stu-id="4d85c-137">Use the **Refresh** button to update and reload the list of remote page targets on the host machine.</span></span> <span data-ttu-id="4d85c-138">Clique no botão **Desconectar** para retornar à tela *conectar-se a um dispositivo remoto e conectar-se* a um host diferente.</span><span class="sxs-lookup"><span data-stu-id="4d85c-138">Click the **Disconnect** button to return to the *Connect to a remote device* screen and attach to a different host.</span></span>

## <span data-ttu-id="4d85c-139">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4d85c-139">Visual Studio Code</span></span>

<span data-ttu-id="4d85c-140">Com o [depurador para Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código, você pode depurar o script executado no Microsoft Edge diretamente no código do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4d85c-140">With the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug script running in Microsoft Edge directly in Visual Studio Code.</span></span> <span data-ttu-id="4d85c-141">A extensão exige que você esteja servindo seu aplicativo Web do localhost, que pode ser iniciado a partir de uma linha de comando ou de uma [tarefa](https://code.visualstudio.com/docs/editor/tasks).</span><span class="sxs-lookup"><span data-stu-id="4d85c-141">The extension requires you to be serving your web application from localhost, which you can start from either command-line or a [Task](https://code.visualstudio.com/docs/editor/tasks).</span></span>

<span data-ttu-id="4d85c-142">Para começar:</span><span class="sxs-lookup"><span data-stu-id="4d85c-142">To get started:</span></span>

1. <span data-ttu-id="4d85c-143">Instale o [depurador para Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs extensão de código.</span><span class="sxs-lookup"><span data-stu-id="4d85c-143">Install the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension.</span></span>

2. <span data-ttu-id="4d85c-144">Reinicie o código VS, abra a pasta que contém o projeto que você deseja depurar e defina os pontos de interrupção no código.</span><span class="sxs-lookup"><span data-stu-id="4d85c-144">Restart VS Code, open the folder containing the project you wish to debug and set breakpoints in your code.</span></span>

3. <span data-ttu-id="4d85c-145">Configure uma [tarefa de inicialização](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) do localhost para abrir a página desejada do seu projeto: **depurar**  >  **Adicionar configuração..**.. Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4d85c-145">Configure a localhost [launch task](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) to open the desired page of your project: **Debug** > **Add Configuration...**. For example:</span></span>

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    <span data-ttu-id="4d85c-146">[*Usar o depurador*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) tem mais opções de configuração de inicialização.</span><span class="sxs-lookup"><span data-stu-id="4d85c-146">[*Using the debugger*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) has more on launch configuration settings.</span></span> 

4. <span data-ttu-id="4d85c-147">Inicie o servidor no localhost e pressione o botão **Iniciar Depuração** (Play) ou `F5` iniciar o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4d85c-147">Start your server on localhost and press the **Start Debugging** (play) button or `F5` to launch Microsoft Edge.</span></span> <span data-ttu-id="4d85c-148">Quando um ponto de interrupção é atingido, você se divide no código VS e pode inspecionar ainda mais e percorrer o código.</span><span class="sxs-lookup"><span data-stu-id="4d85c-148">When a breakpoint is hit, you'll break into VS Code and can further inspect and step through code from there.</span></span>

<span data-ttu-id="4d85c-149">Para saber mais, confira a documentação do [vs-Debugger para Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .</span><span class="sxs-lookup"><span data-stu-id="4d85c-149">For more, check out the [VS Code - Debugger for Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) documentation.</span></span>

## <span data-ttu-id="4d85c-150">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4d85c-150">Microsoft Visual Studio</span></span>

<span data-ttu-id="4d85c-151">Usando a versão do [**Visual Studio**](https://www.visualstudio.com) mais recente (visual Studio 15,8 ou posterior) em execução na [atualização de outubro de 2018 do Windows 10](/windows/uwp/whats-new/windows-10-build-17763), você pode iniciar e depurar o Microsoft Edge a partir do IDE em qualquer projeto do ASP.net ou do .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4d85c-151">Using the latest [**Visual Studio**](https://www.visualstudio.com) version (Visual Studio 15.8 or later) running on [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763), you can launch and debug Microsoft Edge from the IDE on any ASP.NET or .NET Core project.</span></span>

<span data-ttu-id="4d85c-152">Veja aqui como configurar a depuração do Microsoft Edge com o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="4d85c-152">Here's how to set up Microsoft Edge debugging with Visual Studio:</span></span>

1.  <span data-ttu-id="4d85c-153">Instale e inicie o [**Visual Studio**](https://www.visualstudio.com/) (visual Studio 15,8 ou posterior) mais recente.</span><span class="sxs-lookup"><span data-stu-id="4d85c-153">Install and launch the latest [**Visual Studio**](https://www.visualstudio.com/) (Visual Studio 15.8 or later).</span></span>

2. <span data-ttu-id="4d85c-154">Abra um projeto existente do ASP.NET ou do .NET Core ou **crie um novo projeto...** usando um dos modelos do **Visual C#** .net.</span><span class="sxs-lookup"><span data-stu-id="4d85c-154">Open an existing ASP.NET or .NET Core project or **Create new project...** using one of the **Visual C#** .NET templates.</span></span>

3. <span data-ttu-id="4d85c-155">No Gerenciador de **soluções**de projeto, abra os arquivos JavaScript que você deseja depurar e defina pontos de interrupção dentro do IDE da mesma forma que faria com o código do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d85c-155">In the project **Solution Explorer**, open the JavaScript files you wish to debug and set breakpoints within the IDE just as you would with server-side code.</span></span>

4. <span data-ttu-id="4d85c-156">Pressione `F5` para iniciar o Microsoft Edge executando o servidor devtools.</span><span class="sxs-lookup"><span data-stu-id="4d85c-156">Press `F5` to launch Microsoft Edge running the DevTools Server.</span></span> <span data-ttu-id="4d85c-157">Quando um ponto de interrupção é atingido, você pode invadir o Visual Studio e pode inspecionar e percorrer o código aqui.</span><span class="sxs-lookup"><span data-stu-id="4d85c-157">When a breakpoint is hit, you'll break into Visual Studio and can further inspect and step through the code from there.</span></span>
