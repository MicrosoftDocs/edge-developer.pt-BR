---
description: O protocolo Microsoft Edge DevTools versão 0,2 dá suporte aos seguintes pontos de extremidade HTTP.
title: Pontos de extremidade HTTP do Microsoft Edge DevTools Protocol versão 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: cc3d0156d92ab479168e0b588ae2b7c9faa7e58f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561322"
---
# <span data-ttu-id="a7f67-103">Pontos de extremidade HTTP do protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="a7f67-103">DevTools Protocol HTTP Endpoints</span></span>

> [!NOTE]
> <span data-ttu-id="a7f67-104">A versão 0,2 do protocolo Microsoft Edge DevTools funciona apenas na [atualização de outubro de 2018 do Windows 10]() e em versões mais recentes do [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="a7f67-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update]() and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="a7f67-105">O **protocolo DevTools 0,2** dá suporte aos seguintes pontos de extremidade http.</span><span class="sxs-lookup"><span data-stu-id="a7f67-105">**DevTools Protocol 0.2** supports the following HTTP endpoints.</span></span> <span data-ttu-id="a7f67-106">Consulte [usando o protocolo](../index.md#using-the-protocol) para saber mais sobre como se conectar a um processo de conteúdo do navegador e a documentação de [domínios](domains/index.md) para a API completa do protocolo devtools baseado na Web Socket.</span><span class="sxs-lookup"><span data-stu-id="a7f67-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="a7f67-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="a7f67-107">/json/version</span></span>
<span data-ttu-id="a7f67-108">Fornece informações sobre o navegador da máquina hospedeira e qual versão do protocolo DevTools ele suporta.</span><span class="sxs-lookup"><span data-stu-id="a7f67-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="a7f67-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7f67-109">Parameters</span></span>**

*<span data-ttu-id="a7f67-110">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="a7f67-110">None</span></span>*

**<span data-ttu-id="a7f67-111">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="a7f67-111">Return object</span></span>**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
}
```

## <span data-ttu-id="a7f67-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="a7f67-112">/json/protocol</span></span>

<span data-ttu-id="a7f67-113">Fornece toda a superfície de API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="a7f67-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="a7f67-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7f67-114">Parameters</span></span>**

*<span data-ttu-id="a7f67-115">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="a7f67-115">None</span></span>*

**<span data-ttu-id="a7f67-116">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="a7f67-116">Return object</span></span>**

<span data-ttu-id="a7f67-117">Objeto JSON que representa a superfície de API disponível para a versão atual do protocolo.</span><span class="sxs-lookup"><span data-stu-id="a7f67-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="a7f67-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="a7f67-118">/json/list</span></span>

<span data-ttu-id="a7f67-119">Fornece uma lista de candidatos de alvos de página para depuração.</span><span class="sxs-lookup"><span data-stu-id="a7f67-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="a7f67-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7f67-120">Parameters</span></span>**

*<span data-ttu-id="a7f67-121">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="a7f67-121">None</span></span>*

**<span data-ttu-id="a7f67-122">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="a7f67-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="a7f67-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="a7f67-123">/json/close</span></span>

<span data-ttu-id="a7f67-124">Fecha o processo de destino (por exemplo, no Microsoft Edge, fecha a guia página.)</span><span class="sxs-lookup"><span data-stu-id="a7f67-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="a7f67-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7f67-125">Parameters</span></span>**

<span data-ttu-id="a7f67-126">ID de destino</span><span class="sxs-lookup"><span data-stu-id="a7f67-126">Target ID</span></span> 

**<span data-ttu-id="a7f67-127">Objeto de retorno</span><span class="sxs-lookup"><span data-stu-id="a7f67-127">Return object</span></span>**

```
String("Target is closing")
```
