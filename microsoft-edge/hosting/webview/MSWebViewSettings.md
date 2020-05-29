---
description: Define propriedades que habilitam ou desabilitam recursos do WebView
title: Objeto MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560966"
---
# <span data-ttu-id="3124a-104">Objeto MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="3124a-104">MSWebViewSettings object</span></span>

<span data-ttu-id="3124a-105">Define propriedades que habilitam ou desabilitam os recursos do [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="3124a-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>

## <span data-ttu-id="3124a-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3124a-106">Properties</span></span>

### <span data-ttu-id="3124a-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="3124a-107">isIndexedDBEnabled</span></span>

<span data-ttu-id="3124a-108">Obtém ou define um valor que indica se o uso de IndexedDB é permitido no [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="3124a-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### <span data-ttu-id="3124a-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3124a-109">Property value</span></span>
<span data-ttu-id="3124a-110">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3124a-110">Type: **boolean**</span></span>

<span data-ttu-id="3124a-111">**True** se IndexedDB for permitido no **WebView**; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3124a-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span> 

### <span data-ttu-id="3124a-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="3124a-112">isJavaScriptEnabled</span></span>

<span data-ttu-id="3124a-113">Obtém ou define um valor que indica se o uso de JavaScript é permitido no [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="3124a-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### <span data-ttu-id="3124a-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3124a-114">Property value</span></span>
<span data-ttu-id="3124a-115">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3124a-115">Type: **boolean**</span></span>

<span data-ttu-id="3124a-116">**Verdadeiro** O JavaScript é permitido no [WebView](../webview.md); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3124a-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 

### <span data-ttu-id="3124a-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="3124a-117">isScriptNotifyAllowed</span></span>

<span data-ttu-id="3124a-118">Obtém ou define um valor que indica se o uso de [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="3124a-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### <span data-ttu-id="3124a-119">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3124a-119">Property value</span></span>
<span data-ttu-id="3124a-120">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="3124a-120">Type: **boolean**</span></span>

<span data-ttu-id="3124a-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) é permitido no [WebView](../webview.md); caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="3124a-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 
