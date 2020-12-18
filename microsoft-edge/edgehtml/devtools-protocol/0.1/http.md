---
description: O protocolo Microsoft Edge DevTools versão 0,1 dá suporte aos seguintes pontos de extremidade HTTP.
title: DevTools Protocol versão 0,1 de pontos de extremidade HTTP (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5fe50122728304de137efdfb25ebed7274c55cee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231318"
---
# <span data-ttu-id="c4fab-103">DevTools Protocol versão 0,1 de pontos de extremidade HTTP (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="c4fab-103">DevTools Protocol Version 0.1 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="c4fab-104">O protocolo Microsoft Edge DevTools funciona apenas na [atualização de abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="c4fab-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="c4fab-105">O **protocolo DevTools 0,1** dá suporte aos seguintes pontos de extremidade http.</span><span class="sxs-lookup"><span data-stu-id="c4fab-105">**DevTools Protocol 0.1** supports the following HTTP endpoints.</span></span> <span data-ttu-id="c4fab-106">Consulte [usando o protocolo](../index.md#using-the-protocol) para saber mais sobre como se conectar a um processo de conteúdo do navegador e a documentação de [domínios](domains/index.md) para a API completa do protocolo devtools baseado na Web Socket.</span><span class="sxs-lookup"><span data-stu-id="c4fab-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="c4fab-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="c4fab-107">/json/version</span></span>
<span data-ttu-id="c4fab-108">Fornece informações sobre o navegador da máquina hospedeira e qual versão do protocolo DevTools ele suporta.</span><span class="sxs-lookup"><span data-stu-id="c4fab-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="c4fab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4fab-109">Parameters</span></span>**

*<span data-ttu-id="c4fab-110">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c4fab-110">None</span></span>*

**<span data-ttu-id="c4fab-111">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c4fab-111">Return object</span></span>**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## <span data-ttu-id="c4fab-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="c4fab-112">/json/protocol</span></span>

<span data-ttu-id="c4fab-113">Fornece toda a superfície de API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="c4fab-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="c4fab-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4fab-114">Parameters</span></span>**

*<span data-ttu-id="c4fab-115">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c4fab-115">None</span></span>*

**<span data-ttu-id="c4fab-116">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c4fab-116">Return object</span></span>**

<span data-ttu-id="c4fab-117">Objeto JSON que representa a superfície de API disponível para a versão atual do protocolo.</span><span class="sxs-lookup"><span data-stu-id="c4fab-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="c4fab-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="c4fab-118">/json/list</span></span>

<span data-ttu-id="c4fab-119">Fornece uma lista de candidatos de alvos de página para depuração.</span><span class="sxs-lookup"><span data-stu-id="c4fab-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="c4fab-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4fab-120">Parameters</span></span>**

*<span data-ttu-id="c4fab-121">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="c4fab-121">None</span></span>*

**<span data-ttu-id="c4fab-122">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c4fab-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="c4fab-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="c4fab-123">/json/close</span></span>

<span data-ttu-id="c4fab-124">Fecha o processo de destino (por exemplo, no Microsoft Edge, fecha a guia página.)</span><span class="sxs-lookup"><span data-stu-id="c4fab-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="c4fab-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4fab-125">Parameters</span></span>**

<span data-ttu-id="c4fab-126">ID de destino</span><span class="sxs-lookup"><span data-stu-id="c4fab-126">Target ID</span></span> 

**<span data-ttu-id="c4fab-127">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="c4fab-127">Return object</span></span>**

```
String("Target is closing")
```
