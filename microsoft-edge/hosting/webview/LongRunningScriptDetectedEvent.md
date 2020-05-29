---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560975"
---
# <span data-ttu-id="d4af6-103">Objeto LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="d4af6-103">LongRunningScriptDetectedEvent object</span></span>

<span data-ttu-id="d4af6-104">Fornece informações para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="d4af6-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>

## <span data-ttu-id="d4af6-105">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d4af6-105">Properties</span></span>

### <span data-ttu-id="d4af6-106">ExecutionTime</span><span class="sxs-lookup"><span data-stu-id="d4af6-106">executionTime</span></span>

<span data-ttu-id="d4af6-107">Obtém o número de milissegundos durante os quais o elemento [WebView](../webview.md) está executando um script de longa execução.</span><span class="sxs-lookup"><span data-stu-id="d4af6-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### <span data-ttu-id="d4af6-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d4af6-108">Property value</span></span>
<span data-ttu-id="d4af6-109">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="d4af6-109">Type: **long**</span></span>

### <span data-ttu-id="d4af6-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="d4af6-110">stopPageScriptExecution</span></span>
<span data-ttu-id="d4af6-111">Interrompe um script de execução longa em execução no elemento [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="d4af6-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### <span data-ttu-id="d4af6-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d4af6-112">Property value</span></span>
<span data-ttu-id="d4af6-113">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d4af6-113">Type: **Boolean**</span></span>