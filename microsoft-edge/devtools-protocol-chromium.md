---
description: Atualizar para o protocolo Microsoft Edge DevTools
title: Atualização do protocolo Microsoft Edge DevTools
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: f1936a83f948dd17cc76139b7fd67fc73cd692d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561366"
---
# <span data-ttu-id="97798-103">Protocolo de DevTools Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="97798-103">Microsoft Edge (Chromium) DevTools Protocol</span></span>

<span data-ttu-id="97798-104">Com o turno na plataforma da Web subjacente do Microsoft Edge com o Chromium, o [protocolo de devtools do Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) não receberá mais atualizações.</span><span class="sxs-lookup"><span data-stu-id="97798-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) will not be receiving any further updates.</span></span> <span data-ttu-id="97798-105">O protocolo do DevTools do Microsoft Edge (Chromium) corresponderá às APIs do protocolo Chrome DevTools que continuarão no futuro.</span><span class="sxs-lookup"><span data-stu-id="97798-105">The Microsoft Edge (Chromium) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span> 

<span data-ttu-id="97798-106">Você pode encontrar documentação sobre esses domínios e métodos fazendo referência ao Visualizador de [protocolo do Chrome devtools](https://chromedevtools.github.io/devtools-protocol/tot/).</span><span class="sxs-lookup"><span data-stu-id="97798-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot/).</span></span>

> [!NOTE]
> <span data-ttu-id="97798-107">Qualquer método que tenha sido prefixado `ms` no [protocolo devtools Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) não tem mais suporte no protocolo devtools Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="97798-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) are no longer supported in the Microsoft Edge (Chromium) DevTools Protocol.</span></span>

## <span data-ttu-id="97798-108">Usar o protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="97798-108">Using the DevTools Protocol</span></span>

<span data-ttu-id="97798-109">Veja como anexar um cliente de ferramentas personalizado ao servidor DevTools no Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="97798-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge (Chromium).</span></span>

1. <span data-ttu-id="97798-110">Verifique se todas as instâncias do Microsoft Edge (Chromium) estão fechadas.</span><span class="sxs-lookup"><span data-stu-id="97798-110">Ensure all instances of Microsoft Edge (Chromium) are closed.</span></span>

2. <span data-ttu-id="97798-111">Inicie o Microsoft Edge (Chromium) com a porta de depuração remota:</span><span class="sxs-lookup"><span data-stu-id="97798-111">Launch Microsoft Edge (Chromium) with the remote debugging port:</span></span>

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. <span data-ttu-id="97798-112">Opcionalmente, você pode iniciar uma instância separada do Edge usando um perfil de usuário distinto, se desejar:</span><span class="sxs-lookup"><span data-stu-id="97798-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired:</span></span>

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. <span data-ttu-id="97798-113">Em seguida, use o `list` ponto de extremidade http para obter uma lista de destinos de página anexáveis:</span><span class="sxs-lookup"><span data-stu-id="97798-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets:</span></span>

    ```
    http://localhost:9222/json/list
    ```

5. <span data-ttu-id="97798-114">Por fim, conecte-se aos `webSocketDebuggerUrl` comandos de destino e problema desejados/assine mensagens de evento por meio do devtools Web Socket Server.</span><span class="sxs-lookup"><span data-stu-id="97798-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>

## <span data-ttu-id="97798-115">Pontos de extremidade HTTP do protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="97798-115">DevTools Protocol HTTP Endpoints</span></span>

<span data-ttu-id="97798-116">O protocolo DevTools do Microsoft Edge (Chromium) dá suporte aos seguintes pontos de extremidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="97798-116">The Microsoft Edge (Chromium) DevTools Protocol supports the following HTTP endpoints.</span></span>

## <span data-ttu-id="97798-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="97798-117">/json/version</span></span>
<span data-ttu-id="97798-118">Fornece informações sobre o navegador da máquina hospedeira e qual versão do protocolo DevTools ele suporta.</span><span class="sxs-lookup"><span data-stu-id="97798-118">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="97798-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-119">Parameters</span></span>**

*<span data-ttu-id="97798-120">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97798-120">None</span></span>*

**<span data-ttu-id="97798-121">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-121">Return object</span></span>**

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

## <span data-ttu-id="97798-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="97798-122">/json/protocol</span></span>

<span data-ttu-id="97798-123">Fornece toda a superfície de API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="97798-123">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="97798-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-124">Parameters</span></span>**

*<span data-ttu-id="97798-125">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97798-125">None</span></span>*

**<span data-ttu-id="97798-126">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-126">Return object</span></span>**

<span data-ttu-id="97798-127">Objeto JSON que representa a superfície de API disponível para a versão atual do protocolo.</span><span class="sxs-lookup"><span data-stu-id="97798-127">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="97798-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="97798-128">/json/list</span></span>

<span data-ttu-id="97798-129">Fornece uma lista de candidatos de alvos de página para depuração.</span><span class="sxs-lookup"><span data-stu-id="97798-129">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="97798-130">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-130">Parameters</span></span>**

*<span data-ttu-id="97798-131">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97798-131">None</span></span>*

**<span data-ttu-id="97798-132">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-132">Return object</span></span>**

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, … ]
```

## <span data-ttu-id="97798-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="97798-133">/json/close</span></span>

<span data-ttu-id="97798-134">Fecha o processo de destino (por exemplo, no Microsoft Edge (Chromium), fecha a guia página.)</span><span class="sxs-lookup"><span data-stu-id="97798-134">Closes down the target process (e.g., in Microsoft Edge (Chromium), closes the page tab.)</span></span>

**<span data-ttu-id="97798-135">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-135">Parameters</span></span>**

<span data-ttu-id="97798-136">ID de destino</span><span class="sxs-lookup"><span data-stu-id="97798-136">Target ID</span></span> 

**<span data-ttu-id="97798-137">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-137">Return object</span></span>**

```
String(“Target is closing”)
```

## <span data-ttu-id="97798-138">Ferramentas remotas para Microsoft Edge (beta)</span><span class="sxs-lookup"><span data-stu-id="97798-138">Remote Tools for Microsoft Edge (Beta)</span></span>

<span data-ttu-id="97798-139">Agora você pode instalar as [ferramentas remotas para o Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) da [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span><span class="sxs-lookup"><span data-stu-id="97798-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span> <span data-ttu-id="97798-140">Este aplicativo permite que você depure remotamente o Microsoft Edge (Chromium) em execução em um dispositivo com Windows 10 da sua máquina de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="97798-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>

<span data-ttu-id="97798-141">Para saber como configurar seu dispositivo Windows 10 e conectar-se a ele a partir de seu computador de desenvolvimento, confira [este tutorial](./devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="97798-141">To learn how to set up your Windows 10 device and connect to it from your development machine, check out [this tutorial](./devtools-guide-chromium/remote-debugging/windows.md).</span></span>

<span data-ttu-id="97798-142">As [ferramentas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usam o mesmo protocolo devtools Microsoft Edge (Chromium) que o [devtools](./devtools-guide-chromium.md) para se comunicar com o Microsoft Edge em execução no dispositivo Windows 10 que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="97798-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](./devtools-guide-chromium.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span> <span data-ttu-id="97798-143">Esse aplicativo apenas precede `/msedge/` e uma ID de processo ( `pid` ) antes de cada chamada para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="97798-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span> <span data-ttu-id="97798-144">Ele é compatível com os seguintes pontos de extremidade HTTP.</span><span class="sxs-lookup"><span data-stu-id="97798-144">It supports the following HTTP endpoints.</span></span>

### <span data-ttu-id="97798-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="97798-145">/msedge/json/list</span></span>

<span data-ttu-id="97798-146">Fornece uma lista de candidatos a todos os `msedge.exe` processos (incluindo [PWAs](./progressive-web-apps-chromium/index.md) e todas as guias em todas as instâncias do Microsoft Edge) no dispositivo Windows 10 para depuração.</span><span class="sxs-lookup"><span data-stu-id="97798-146">Provides a candidate list of all `msedge.exe` processes (including [PWAs](./progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge) on the Windows 10 device for debugging.</span></span>

**<span data-ttu-id="97798-147">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-147">Parameters</span></span>**

*<span data-ttu-id="97798-148">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97798-148">None</span></span>*

**<span data-ttu-id="97798-149">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-149">Return object</span></span>**

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
}, … ]
```

### <span data-ttu-id="97798-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="97798-150">/msedge/</span></span>

<span data-ttu-id="97798-151">Funcionalmente equivalente a [/msedge/JSON/List](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="97798-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span> 

### <span data-ttu-id="97798-152">/msedge/[pid]/JSON/List</span><span class="sxs-lookup"><span data-stu-id="97798-152">/msedge/[pid]/json/list</span></span>

<span data-ttu-id="97798-153">Fornece uma lista de candidatos de destinos de página para a instância do Microsoft Edge que corresponde à fornecida `[pid]` para depuração.</span><span class="sxs-lookup"><span data-stu-id="97798-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>

**<span data-ttu-id="97798-154">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-154">Parameters</span></span>**

*<span data-ttu-id="97798-155">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97798-155">None</span></span>*

**<span data-ttu-id="97798-156">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-156">Return object</span></span>**

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
}, … ]
```

### <span data-ttu-id="97798-157">/msedge/[pid]/JSON/Version</span><span class="sxs-lookup"><span data-stu-id="97798-157">/msedge/[pid]/json/version</span></span>

<span data-ttu-id="97798-158">Fornece informações sobre a instância do Microsoft Edge que corresponde ao fornecido `[pid]` e à versão do protocolo devtools que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="97798-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="97798-159">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-159">Parameters</span></span>**

*<span data-ttu-id="97798-160">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97798-160">None</span></span>*

**<span data-ttu-id="97798-161">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-161">Return object</span></span>**

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

### <span data-ttu-id="97798-162">/msedge/[pid]/JSON/Protocol/</span><span class="sxs-lookup"><span data-stu-id="97798-162">/msedge/[pid]/json/protocol/</span></span>

<span data-ttu-id="97798-163">Fornece a superfície de API de protocolo inteira serializada como JSON para a instância do Microsoft Edge que corresponde ao fornecido `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="97798-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>

**<span data-ttu-id="97798-164">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97798-164">Parameters</span></span>**

*<span data-ttu-id="97798-165">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="97798-165">None</span></span>*

**<span data-ttu-id="97798-166">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="97798-166">Return object</span></span>**

<span data-ttu-id="97798-167">Objeto JSON que representa a superfície de API disponível para a versão do protocolo que a instância do Microsoft Edge correspondente à fornecida `[pid]` está usando.</span><span class="sxs-lookup"><span data-stu-id="97798-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>
