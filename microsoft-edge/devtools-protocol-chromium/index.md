---
description: Atualizar para o protocolo Microsoft Edge DevTools
title: Microsoft Edge Atualização do Protocolo DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: de7d6c39c09ba321f21b34e6e461ec030f09f6ad
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480157"
---
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a><span data-ttu-id="9329d-103">Microsoft Edge (Chromium) Visão geral do Protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="9329d-103">Microsoft Edge (Chromium) DevTools Protocol overview</span></span>  

<span data-ttu-id="9329d-104">Com a mudança na plataforma Web subjacente de Microsoft Edge para Chromium, o Protocolo [Microsoft Edge (EdgeHTML) DevTools não](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) receberá mais atualizações.</span><span class="sxs-lookup"><span data-stu-id="9329d-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) will not be receiving any further updates.</span></span>  <span data-ttu-id="9329d-105">O Microsoft Edge \(Chromium\) Protocolo DevTools corresponderá às APIs do Protocolo Chrome DevTools em frente.</span><span class="sxs-lookup"><span data-stu-id="9329d-105">The Microsoft Edge \(Chromium\) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span>  

<span data-ttu-id="9329d-106">Você pode encontrar documentação sobre esses domínios e métodos referindo-se ao Visualizador de Protocolo [Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot).</span><span class="sxs-lookup"><span data-stu-id="9329d-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot).</span></span>  

> [!NOTE]
> <span data-ttu-id="9329d-107">Todos os métodos que foram prefixados no protocolo `ms` [Microsoft Edge (EdgeHTML) DevTools](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) não são mais suportados no protocolo Microsoft Edge \(Chromium\) DevTools Protocol.</span><span class="sxs-lookup"><span data-stu-id="9329d-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) are no longer supported in the Microsoft Edge \(Chromium\) DevTools Protocol.</span></span>  

## <a name="using-the-devtools-protocol"></a><span data-ttu-id="9329d-108">Usando o Protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="9329d-108">Using the DevTools Protocol</span></span>  

<span data-ttu-id="9329d-109">Veja como anexar um cliente de ferramentas personalizado ao Servidor DevTools em Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="9329d-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge \(Chromium\).</span></span>  

1.  <span data-ttu-id="9329d-110">Verifique se todas as instâncias de Microsoft Edge \(Chromium\) estão fechadas.</span><span class="sxs-lookup"><span data-stu-id="9329d-110">Ensure all instances of Microsoft Edge \(Chromium\) are closed.</span></span>  
1.  <span data-ttu-id="9329d-111">Iniciar Microsoft Edge \(Chromium\) com a porta de depuração remota:.</span><span class="sxs-lookup"><span data-stu-id="9329d-111">Launch Microsoft Edge \(Chromium\) with the remote debugging port:.</span></span> 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="9329d-112">Opcionalmente, você pode iniciar uma instância separada do Edge usando um perfil de usuário distinto, se desejado.</span><span class="sxs-lookup"><span data-stu-id="9329d-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired.</span></span>  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  <span data-ttu-id="9329d-113">Em seguida, use o ponto de extremidade HTTP `list` para obter uma lista de destinos de página anexados.</span><span class="sxs-lookup"><span data-stu-id="9329d-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets.</span></span>  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  <span data-ttu-id="9329d-114">Por fim, conecte-se ao dos comandos de destino e de emissão desejados/inscreva-se nas mensagens de evento por meio do servidor `webSocketDebuggerUrl` de soquete web DevTools.</span><span class="sxs-lookup"><span data-stu-id="9329d-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>  

## <a name="devtools-protocol-http-endpoints"></a><span data-ttu-id="9329d-115">Pontos de extremidade HTTP do Protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="9329d-115">DevTools Protocol HTTP Endpoints</span></span>  

<span data-ttu-id="9329d-116">O Microsoft Edge \(Chromium\) Protocolo DevTools oferece suporte aos seguintes pontos de extremidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="9329d-116">The Microsoft Edge \(Chromium\) DevTools Protocol supports the following HTTP endpoints.</span></span>  

## <a name="jsonversion"></a><span data-ttu-id="9329d-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="9329d-117">/json/version</span></span>  

<span data-ttu-id="9329d-118">Fornece informações sobre o navegador do computador host e qual versão do Protocolo DevTools suporta.</span><span class="sxs-lookup"><span data-stu-id="9329d-118">Provides information on the browser of the host machine and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="9329d-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-119">Parameters</span></span>**  

**<span data-ttu-id="9329d-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9329d-120">None</span></span>**  

**<span data-ttu-id="9329d-121">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-121">Return object</span></span>**  

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

## <a name="jsonprotocol"></a><span data-ttu-id="9329d-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="9329d-122">/json/protocol</span></span>  

<span data-ttu-id="9329d-123">Fornece toda a superfície da API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="9329d-123">Provides the entire protocol API surface serialized as JSON.</span></span>  

**<span data-ttu-id="9329d-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-124">Parameters</span></span>**  

**<span data-ttu-id="9329d-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9329d-125">None</span></span>**  

**<span data-ttu-id="9329d-126">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-126">Return object</span></span>**  

<span data-ttu-id="9329d-127">Objeto JSON que representa a superfície da API disponível para a versão atual do protocolo.</span><span class="sxs-lookup"><span data-stu-id="9329d-127">JSON object which represents the available API surface for current version of the protocol.</span></span>  

## <a name="jsonlist"></a><span data-ttu-id="9329d-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="9329d-128">/json/list</span></span>  

<span data-ttu-id="9329d-129">Fornece uma lista de candidatos de destinos de página para depuração.</span><span class="sxs-lookup"><span data-stu-id="9329d-129">Provides a candidate list of page targets for debugging.</span></span>  

**<span data-ttu-id="9329d-130">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-130">Parameters</span></span>**  

**<span data-ttu-id="9329d-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9329d-131">None</span></span>**  

**<span data-ttu-id="9329d-132">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-132">Return object</span></span>**  

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

## <a name="jsonclose"></a><span data-ttu-id="9329d-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="9329d-133">/json/close</span></span>  

<span data-ttu-id="9329d-134">Fecha o processo de destino \(por exemplo, em Microsoft Edge \(Chromium\), fecha a guia página\).</span><span class="sxs-lookup"><span data-stu-id="9329d-134">Closes down the target process \(for example, in Microsoft Edge \(Chromium\), closes the page tab\).</span></span>  

**<span data-ttu-id="9329d-135">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-135">Parameters</span></span>**  

<span data-ttu-id="9329d-136">ID de destino</span><span class="sxs-lookup"><span data-stu-id="9329d-136">Target ID</span></span>  

**<span data-ttu-id="9329d-137">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-137">Return object</span></span>**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a><span data-ttu-id="9329d-138">Ferramentas remotas para Microsoft Edge (Beta)</span><span class="sxs-lookup"><span data-stu-id="9329d-138">Remote Tools for Microsoft Edge (Beta)</span></span>  

<span data-ttu-id="9329d-139">Agora você pode instalar as Ferramentas Remotas para [Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) do [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span><span class="sxs-lookup"><span data-stu-id="9329d-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span>  <span data-ttu-id="9329d-140">Este aplicativo permite que você depure remotamente Microsoft Edge (Chromium) em execução em um dispositivo Windows 10 de seu computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="9329d-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>  

<span data-ttu-id="9329d-141">Para saber como configurar seu dispositivo Windows 10 e se conectar a ele a partir de sua máquina de desenvolvimento, navegue até Introdução com a [Depuração Remota Windows 10 Dispositivos](../devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="9329d-141">To learn how to set up your Windows 10 device and connect to it from your development machine, navigate to [Get Started with Remote Debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).</span></span>  

<span data-ttu-id="9329d-142">As Ferramentas Remotas para [Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usam o mesmo protocolo Microsoft Edge (Chromium) DevTools que o [DevTools](../devtools-guide-chromium/index.md) para se comunicar com Microsoft Edge em execução no dispositivo Windows 10 que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="9329d-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](../devtools-guide-chromium/index.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span>  <span data-ttu-id="9329d-143">Este aplicativo apenas se prepara e `/msedge/` uma ID do processo ( `pid` ) antes de cada chamada para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="9329d-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span>  <span data-ttu-id="9329d-144">Ele dá suporte aos seguintes pontos de extremidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="9329d-144">It supports the following HTTP endpoints.</span></span>  

### <a name="msedgejsonlist"></a><span data-ttu-id="9329d-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="9329d-145">/msedge/json/list</span></span>  

<span data-ttu-id="9329d-146">Fornece uma lista de candidatos de todos os processos `msedge.exe` \(incluindo [PWAs](../progressive-web-apps-chromium/index.md) e todas as guias em todas as instâncias de Microsoft Edge\) no dispositivo Windows 10 para depuração.</span><span class="sxs-lookup"><span data-stu-id="9329d-146">Provides a candidate list of all `msedge.exe` processes \(including [PWAs](../progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge\) on the Windows 10 device for debugging.</span></span>  

**<span data-ttu-id="9329d-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-147">Parameters</span></span>**  

**<span data-ttu-id="9329d-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9329d-148">None</span></span>**  

**<span data-ttu-id="9329d-149">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-149">Return object</span></span>**  

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

### <a name="msedge"></a><span data-ttu-id="9329d-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="9329d-150">/msedge/</span></span>  

<span data-ttu-id="9329d-151">Funcionalmente equivalente a [/msedge/json/list](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="9329d-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span>  

### <a name="msedgepidjsonlist"></a><span data-ttu-id="9329d-152">/msedge/[pid]/json/list</span><span class="sxs-lookup"><span data-stu-id="9329d-152">/msedge/[pid]/json/list</span></span>  

<span data-ttu-id="9329d-153">Fornece uma lista de candidatos de destinos de página para a instância Microsoft Edge que corresponde à `[pid]` fornecida para depuração.</span><span class="sxs-lookup"><span data-stu-id="9329d-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>  

**<span data-ttu-id="9329d-154">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-154">Parameters</span></span>**  

**<span data-ttu-id="9329d-155">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9329d-155">None</span></span>**  

**<span data-ttu-id="9329d-156">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-156">Return object</span></span>**  

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

### <a name="msedgepidjsonversion"></a><span data-ttu-id="9329d-157">/msedge/[pid]/json/version</span><span class="sxs-lookup"><span data-stu-id="9329d-157">/msedge/[pid]/json/version</span></span>  

<span data-ttu-id="9329d-158">Fornece informações sobre a instância Microsoft Edge que corresponde à fornecida e qual versão do `[pid]` Protocolo DevTools ele oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="9329d-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="9329d-159">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-159">Parameters</span></span>**  

**<span data-ttu-id="9329d-160">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9329d-160">None</span></span>**  

**<span data-ttu-id="9329d-161">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-161">Return object</span></span>**  

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

### <a name="msedgepidjsonprotocol"></a><span data-ttu-id="9329d-162">/msedge/[pid]/json/protocol/</span><span class="sxs-lookup"><span data-stu-id="9329d-162">/msedge/[pid]/json/protocol/</span></span>  

<span data-ttu-id="9329d-163">Fornece toda a superfície da API de protocolo serializada como JSON para a instância Microsoft Edge que corresponde à `[pid]` fornecida .</span><span class="sxs-lookup"><span data-stu-id="9329d-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>  

**<span data-ttu-id="9329d-164">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9329d-164">Parameters</span></span>**  

**<span data-ttu-id="9329d-165">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9329d-165">None</span></span>**  

**<span data-ttu-id="9329d-166">Objeto Return</span><span class="sxs-lookup"><span data-stu-id="9329d-166">Return object</span></span>**  

<span data-ttu-id="9329d-167">Objeto JSON que representa a superfície da API disponível para a versão do protocolo que a instância Microsoft Edge que corresponde à `[pid]` fornecida está usando.</span><span class="sxs-lookup"><span data-stu-id="9329d-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>  
