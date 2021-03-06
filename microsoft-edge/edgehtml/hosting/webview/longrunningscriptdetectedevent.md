---
description: Objeto LongRunningScriptDetectedEvent
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: webview, aplicativos do Windows 10, uwp, borda
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397935"
---
# <a name="longrunningscriptdetectedevent-object"></a><span data-ttu-id="f8baa-104">Objeto LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="f8baa-104">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="f8baa-105">Fornece informações para [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="f8baa-105">Provides information for [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span></span>  

## <a name="properties"></a><span data-ttu-id="f8baa-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f8baa-106">Properties</span></span>  

### <a name="executiontime"></a><span data-ttu-id="f8baa-107">executionTime</span><span class="sxs-lookup"><span data-stu-id="f8baa-107">executionTime</span></span>  

<span data-ttu-id="f8baa-108">Obtém o número de milissegundos que o [elemento Webview](../webview/index.md) está executando um script de longa execução.</span><span class="sxs-lookup"><span data-stu-id="f8baa-108">Gets the number of milliseconds that the [webview](../webview/index.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a><span data-ttu-id="f8baa-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f8baa-109">Property value</span></span>  

<span data-ttu-id="f8baa-110">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="f8baa-110">Type: **long**</span></span>  

### <a name="stoppagescriptexecution"></a><span data-ttu-id="f8baa-111">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="f8baa-111">stopPageScriptExecution</span></span>  

<span data-ttu-id="f8baa-112">Interrompe a execução de um script de longa duração no [elemento webview.](../webview/index.md)</span><span class="sxs-lookup"><span data-stu-id="f8baa-112">Stops a long-running script executing in the [webview](../webview/index.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a><span data-ttu-id="f8baa-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f8baa-113">Property value</span></span>  

<span data-ttu-id="f8baa-114">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="f8baa-114">Type: **Boolean**</span></span>  
