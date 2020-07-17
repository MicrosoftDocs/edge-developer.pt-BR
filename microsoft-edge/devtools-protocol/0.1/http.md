---
description: O protocolo Microsoft Edge DevTools versão 0,1 dá suporte aos seguintes pontos de extremidade HTTP.
title: DevTools Protocol versão 0,1 de pontos de extremidade HTTP (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a9d40772b8175790c034ee67236c4887d0831785
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882867"
---
# <span data-ttu-id="6db6b-103">DevTools Protocol versão 0,1 de pontos de extremidade HTTP (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="6db6b-103">DevTools Protocol Version 0.1 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="6db6b-104">O protocolo Microsoft Edge DevTools funciona apenas na [atualização de abril de 2018 do Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="6db6b-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="6db6b-105">O **protocolo DevTools 0,1** dá suporte aos seguintes pontos de extremidade http.</span><span class="sxs-lookup"><span data-stu-id="6db6b-105">**DevTools Protocol 0.1** supports the following HTTP endpoints.</span></span> <span data-ttu-id="6db6b-106">Consulte [usando o protocolo](../index.md#using-the-protocol) para saber mais sobre como se conectar a um processo de conteúdo do navegador e a documentação de [domínios](domains/index.md) para a API completa do protocolo devtools baseado na Web Socket.</span><span class="sxs-lookup"><span data-stu-id="6db6b-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="6db6b-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="6db6b-107">/json/version</span></span>
<span data-ttu-id="6db6b-108">Fornece informações sobre o navegador da máquina hospedeira e qual versão do protocolo DevTools ele suporta.</span><span class="sxs-lookup"><span data-stu-id="6db6b-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="6db6b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6db6b-109">Parameters</span></span>**

*<span data-ttu-id="6db6b-110">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="6db6b-110">None</span></span>*

**<span data-ttu-id="6db6b-111">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="6db6b-111">Return object</span></span>**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## <span data-ttu-id="6db6b-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="6db6b-112">/json/protocol</span></span>

<span data-ttu-id="6db6b-113">Fornece toda a superfície de API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="6db6b-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="6db6b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6db6b-114">Parameters</span></span>**

*<span data-ttu-id="6db6b-115">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="6db6b-115">None</span></span>*

**<span data-ttu-id="6db6b-116">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="6db6b-116">Return object</span></span>**

<span data-ttu-id="6db6b-117">Objeto JSON que representa a superfície de API disponível para a versão atual do protocolo.</span><span class="sxs-lookup"><span data-stu-id="6db6b-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="6db6b-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="6db6b-118">/json/list</span></span>

<span data-ttu-id="6db6b-119">Fornece uma lista de candidatos de alvos de página para depuração.</span><span class="sxs-lookup"><span data-stu-id="6db6b-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="6db6b-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6db6b-120">Parameters</span></span>**

*<span data-ttu-id="6db6b-121">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="6db6b-121">None</span></span>*

**<span data-ttu-id="6db6b-122">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="6db6b-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="6db6b-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="6db6b-123">/json/close</span></span>

<span data-ttu-id="6db6b-124">Fecha o processo de destino (por exemplo, no Microsoft Edge, fecha a guia página.)</span><span class="sxs-lookup"><span data-stu-id="6db6b-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="6db6b-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6db6b-125">Parameters</span></span>**

<span data-ttu-id="6db6b-126">ID de destino</span><span class="sxs-lookup"><span data-stu-id="6db6b-126">Target ID</span></span> 

**<span data-ttu-id="6db6b-127">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="6db6b-127">Return object</span></span>**

```
String("Target is closing")
```
