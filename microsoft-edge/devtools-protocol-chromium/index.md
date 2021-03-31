---
description: Atualizar para o protocolo Microsoft Edge DevTools
title: Atualização do protocolo Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 15b13e2b93d1dbd013a82ea52b643071fa5b6f7e
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231728"
---
# <span data-ttu-id="c1791-103">Visão geral do protocolo DevTools Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="c1791-103">Microsoft Edge (Chromium) DevTools Protocol overview</span></span>  

<span data-ttu-id="c1791-104">Com o turno na plataforma da Web subjacente do Microsoft Edge com o Chromium, o [protocolo de devtools do Microsoft Edge (EdgeHTML)](../edgehtml/devtools-protocol/index.md) não receberá mais atualizações.</span><span class="sxs-lookup"><span data-stu-id="c1791-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](../edgehtml/devtools-protocol/index.md) will not be receiving any further updates.</span></span>  <span data-ttu-id="c1791-105">O protocolo DevTools do Microsoft Edge \(Chromium \) corresponderá às APIs do protocolo Chrome DevTools em andamento.</span><span class="sxs-lookup"><span data-stu-id="c1791-105">The Microsoft Edge \(Chromium\) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span>  

<span data-ttu-id="c1791-106">Você pode encontrar documentação sobre esses domínios e métodos fazendo referência ao Visualizador de [protocolo do Chrome devtools](https://chromedevtools.github.io/devtools-protocol/tot/).</span><span class="sxs-lookup"><span data-stu-id="c1791-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot/).</span></span>  

> [!NOTE]
> <span data-ttu-id="c1791-107">Qualquer método que tenha sido prefixado `ms` no [protocolo devtools Microsoft Edge (EdgeHTML)](../edgehtml/devtools-protocol/index.md) não tem mais suporte no protocolo devtools do Microsoft Edge \(Chromium \).</span><span class="sxs-lookup"><span data-stu-id="c1791-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](../edgehtml/devtools-protocol/index.md) are no longer supported in the Microsoft Edge \(Chromium\) DevTools Protocol.</span></span>  

## <span data-ttu-id="c1791-108">Usar o protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="c1791-108">Using the DevTools Protocol</span></span>  

<span data-ttu-id="c1791-109">Veja como anexar um cliente de ferramentas personalizado ao servidor DevTools no Microsoft Edge \(Chromium \).</span><span class="sxs-lookup"><span data-stu-id="c1791-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge \(Chromium\).</span></span>  

1.  <span data-ttu-id="c1791-110">Verifique se todas as instâncias do Microsoft Edge \(Chromium \) estão fechadas.</span><span class="sxs-lookup"><span data-stu-id="c1791-110">Ensure all instances of Microsoft Edge \(Chromium\) are closed.</span></span>  
1.  <span data-ttu-id="c1791-111">Inicie o Microsoft Edge \(Chromium \) com a porta de depuração remota:.</span><span class="sxs-lookup"><span data-stu-id="c1791-111">Launch Microsoft Edge \(Chromium\) with the remote debugging port:.</span></span> 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="c1791-112">Opcionalmente, você pode iniciar uma instância separada do Edge usando um perfil de usuário distinto, se desejado.</span><span class="sxs-lookup"><span data-stu-id="c1791-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired.</span></span>  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  <span data-ttu-id="c1791-113">Em seguida, use o `list` ponto de extremidade http para obter uma lista de destinos de página anexáveis.</span><span class="sxs-lookup"><span data-stu-id="c1791-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets.</span></span>  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  <span data-ttu-id="c1791-114">Por fim, conecte-se aos `webSocketDebuggerUrl` comandos de destino e problema desejados/assine mensagens de evento por meio do devtools Web Socket Server.</span><span class="sxs-lookup"><span data-stu-id="c1791-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>  

## <span data-ttu-id="c1791-115">Pontos de extremidade HTTP do protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="c1791-115">DevTools Protocol HTTP Endpoints</span></span>  

<span data-ttu-id="c1791-116">O protocolo DevTools do Microsoft Edge \(Chromium \) dá suporte aos seguintes pontos de extremidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1791-116">The Microsoft Edge \(Chromium\) DevTools Protocol supports the following HTTP endpoints.</span></span>  

## <span data-ttu-id="c1791-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="c1791-117">/json/version</span></span>  

<span data-ttu-id="c1791-118">Fornece informações sobre o navegador do computador host e qual versão do protocolo DevTools ele suporta.</span><span class="sxs-lookup"><span data-stu-id="c1791-118">Provides information on the browser of the host machine and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="c1791-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-119">Parameters</span></span>**  

**<span data-ttu-id="c1791-120">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c1791-120">None</span></span>**  

**<span data-ttu-id="c1791-121">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-121">Return object</span></span>**  

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
}
```  

## <span data-ttu-id="c1791-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="c1791-122">/json/protocol</span></span>  

<span data-ttu-id="c1791-123">Fornece toda a superfície de API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="c1791-123">Provides the entire protocol API surface serialized as JSON.</span></span>  

**<span data-ttu-id="c1791-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-124">Parameters</span></span>**  

**<span data-ttu-id="c1791-125">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c1791-125">None</span></span>**  

**<span data-ttu-id="c1791-126">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-126">Return object</span></span>**  

<span data-ttu-id="c1791-127">Objeto JSON que representa a superfície de API disponível para a versão atual do protocolo.</span><span class="sxs-lookup"><span data-stu-id="c1791-127">JSON object which represents the available API surface for current version of the protocol.</span></span>  

## <span data-ttu-id="c1791-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="c1791-128">/json/list</span></span>  

<span data-ttu-id="c1791-129">Fornece uma lista de candidatos de alvos de página para depuração.</span><span class="sxs-lookup"><span data-stu-id="c1791-129">Provides a candidate list of page targets for debugging.</span></span>  

**<span data-ttu-id="c1791-130">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-130">Parameters</span></span>**  

**<span data-ttu-id="c1791-131">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c1791-131">None</span></span>**  

**<span data-ttu-id="c1791-132">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-132">Return object</span></span>**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## <span data-ttu-id="c1791-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="c1791-133">/json/close</span></span>  

<span data-ttu-id="c1791-134">Fecha o processo de destino \(por exemplo, no Microsoft Edge \(Chromium \), fecha a guia da página \).</span><span class="sxs-lookup"><span data-stu-id="c1791-134">Closes down the target process \(for example, in Microsoft Edge \(Chromium\), closes the page tab\).</span></span>  

**<span data-ttu-id="c1791-135">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-135">Parameters</span></span>**  

<span data-ttu-id="c1791-136">ID de destino</span><span class="sxs-lookup"><span data-stu-id="c1791-136">Target ID</span></span>  

**<span data-ttu-id="c1791-137">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-137">Return object</span></span>**  

```
String(“Target is closing”)
```  

## <span data-ttu-id="c1791-138">Ferramentas remotas para Microsoft Edge (beta)</span><span class="sxs-lookup"><span data-stu-id="c1791-138">Remote Tools for Microsoft Edge (Beta)</span></span>  

<span data-ttu-id="c1791-139">Agora você pode instalar as [ferramentas remotas para o Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) da [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span><span class="sxs-lookup"><span data-stu-id="c1791-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span>  <span data-ttu-id="c1791-140">Este aplicativo permite que você depure remotamente o Microsoft Edge (Chromium) em execução em um dispositivo com Windows 10 da sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="c1791-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>  

<span data-ttu-id="c1791-141">Para saber como configurar seu dispositivo Windows 10 e conectar-se a ele a partir de seu computador de desenvolvimento, navegue até [introdução à depuração remota de dispositivos Windows 10](../devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="c1791-141">To learn how to set up your Windows 10 device and connect to it from your development machine, navigate to [Get Started with Remote Debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).</span></span>  

<span data-ttu-id="c1791-142">As [ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usam o mesmo protocolo devtools Microsoft Edge (Chromium) que o [devtools](../devtools-guide-chromium/index.md) para se comunicar com o Microsoft Edge em execução no dispositivo Windows 10 que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="c1791-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](../devtools-guide-chromium/index.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span>  <span data-ttu-id="c1791-143">Esse aplicativo apenas precede `/msedge/` e uma ID de processo ( `pid` ) antes de cada chamada para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="c1791-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span>  <span data-ttu-id="c1791-144">Ele é compatível com os seguintes pontos de extremidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="c1791-144">It supports the following HTTP endpoints.</span></span>  

### <span data-ttu-id="c1791-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="c1791-145">/msedge/json/list</span></span>  

<span data-ttu-id="c1791-146">Fornece uma lista de candidatos de todos os `msedge.exe` processos \(incluindo [PWAs](../progressive-web-apps-chromium/index.md) e todas as guias em todas as instâncias do Microsoft Edge \) no dispositivo Windows 10 para depuração.</span><span class="sxs-lookup"><span data-stu-id="c1791-146">Provides a candidate list of all `msedge.exe` processes \(including [PWAs](../progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge\) on the Windows 10 device for debugging.</span></span>  

**<span data-ttu-id="c1791-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-147">Parameters</span></span>**  

**<span data-ttu-id="c1791-148">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c1791-148">None</span></span>**  

**<span data-ttu-id="c1791-149">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-149">Return object</span></span>**  

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, ...  ]
```  

### <span data-ttu-id="c1791-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="c1791-150">/msedge/</span></span>  

<span data-ttu-id="c1791-151">Funcionalmente equivalente a [/msedge/JSON/List](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="c1791-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span>  

### <span data-ttu-id="c1791-152">/msedge/[pid]/JSON/List</span><span class="sxs-lookup"><span data-stu-id="c1791-152">/msedge/[pid]/json/list</span></span>  

<span data-ttu-id="c1791-153">Fornece uma lista de candidatos de destinos de página para a instância do Microsoft Edge que corresponde à fornecida `[pid]` para depuração.</span><span class="sxs-lookup"><span data-stu-id="c1791-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>  

**<span data-ttu-id="c1791-154">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-154">Parameters</span></span>**  

**<span data-ttu-id="c1791-155">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c1791-155">None</span></span>**  

**<span data-ttu-id="c1791-156">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-156">Return object</span></span>**  

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, ...  ]
```  

### <span data-ttu-id="c1791-157">/msedge/[pid]/JSON/Version</span><span class="sxs-lookup"><span data-stu-id="c1791-157">/msedge/[pid]/json/version</span></span>  

<span data-ttu-id="c1791-158">Fornece informações sobre a instância do Microsoft Edge que corresponde ao fornecido `[pid]` e à versão do protocolo devtools que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="c1791-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="c1791-159">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-159">Parameters</span></span>**  

**<span data-ttu-id="c1791-160">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c1791-160">None</span></span>**  

**<span data-ttu-id="c1791-161">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-161">Return object</span></span>**  

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```  

### <span data-ttu-id="c1791-162">/msedge/[pid]/JSON/Protocol/</span><span class="sxs-lookup"><span data-stu-id="c1791-162">/msedge/[pid]/json/protocol/</span></span>  

<span data-ttu-id="c1791-163">Fornece a superfície de API de protocolo inteira serializada como JSON para a instância do Microsoft Edge que corresponde ao fornecido `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="c1791-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>  

**<span data-ttu-id="c1791-164">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1791-164">Parameters</span></span>**  

**<span data-ttu-id="c1791-165">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c1791-165">None</span></span>**  

**<span data-ttu-id="c1791-166">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c1791-166">Return object</span></span>**  

<span data-ttu-id="c1791-167">Objeto JSON que representa a superfície de API disponível para a versão do protocolo que a instância do Microsoft Edge correspondente à fornecida `[pid]` está usando.</span><span class="sxs-lookup"><span data-stu-id="c1791-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>  
