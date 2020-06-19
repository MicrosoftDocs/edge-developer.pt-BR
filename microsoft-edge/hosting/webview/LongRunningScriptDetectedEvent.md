---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752147"
---
# <span data-ttu-id="78e6a-103">Objeto LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="78e6a-103">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="78e6a-104">Fornece informações para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="78e6a-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>  

## <span data-ttu-id="78e6a-105">Propriedades</span><span class="sxs-lookup"><span data-stu-id="78e6a-105">Properties</span></span>  

### <span data-ttu-id="78e6a-106">ExecutionTime</span><span class="sxs-lookup"><span data-stu-id="78e6a-106">executionTime</span></span>  

<span data-ttu-id="78e6a-107">Obtém o número de milissegundos durante os quais o elemento [WebView](../webview.md) está executando um script de longa execução.</span><span class="sxs-lookup"><span data-stu-id="78e6a-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <span data-ttu-id="78e6a-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="78e6a-108">Property value</span></span>  

<span data-ttu-id="78e6a-109">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="78e6a-109">Type: **long**</span></span>  

### <span data-ttu-id="78e6a-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="78e6a-110">stopPageScriptExecution</span></span>  

<span data-ttu-id="78e6a-111">Interrompe um script de execução longa em execução no elemento [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="78e6a-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <span data-ttu-id="78e6a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="78e6a-112">Property value</span></span>  

<span data-ttu-id="78e6a-113">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="78e6a-113">Type: **Boolean**</span></span>  
