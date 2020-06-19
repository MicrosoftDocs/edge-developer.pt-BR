---
description: Define propriedades que habilitam ou desabilitam recursos do WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752175"
---
# <span data-ttu-id="3f5a0-104">Objeto MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="3f5a0-104">MSWebViewSettings object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="3f5a0-105">Define propriedades que habilitam ou desabilitam os recursos do [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="3f5a0-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>  

## <span data-ttu-id="3f5a0-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3f5a0-106">Properties</span></span>  

### <span data-ttu-id="3f5a0-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="3f5a0-107">isIndexedDBEnabled</span></span>  

<span data-ttu-id="3f5a0-108">Obtém ou define um valor que indica se o uso de IndexedDB é permitido no [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="3f5a0-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### <span data-ttu-id="3f5a0-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3f5a0-109">Property value</span></span>  

<span data-ttu-id="3f5a0-110">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3f5a0-110">Type: **boolean**</span></span>  

<span data-ttu-id="3f5a0-111">**True** se IndexedDB for permitido no **WebView**; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3f5a0-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span>  

### <span data-ttu-id="3f5a0-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="3f5a0-112">isJavaScriptEnabled</span></span>  

<span data-ttu-id="3f5a0-113">Obtém ou define um valor que indica se o uso de JavaScript é permitido no [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="3f5a0-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### <span data-ttu-id="3f5a0-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3f5a0-114">Property value</span></span>  

<span data-ttu-id="3f5a0-115">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3f5a0-115">Type: **boolean**</span></span>  

<span data-ttu-id="3f5a0-116">**Verdadeiro** O JavaScript é permitido no [WebView](../webview.md); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3f5a0-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  

### <span data-ttu-id="3f5a0-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="3f5a0-117">isScriptNotifyAllowed</span></span>  

<span data-ttu-id="3f5a0-118">Obtém ou define um valor que indica se o uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="3f5a0-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### <span data-ttu-id="3f5a0-119">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3f5a0-119">Property value</span></span>  

<span data-ttu-id="3f5a0-120">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3f5a0-120">Type: **boolean**</span></span>  

<span data-ttu-id="3f5a0-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3f5a0-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  
