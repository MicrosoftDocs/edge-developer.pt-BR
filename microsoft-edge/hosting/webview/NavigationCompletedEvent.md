---
description: Contém informações sobre a navegação da WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560965"
---
# <span data-ttu-id="410ce-104">Objeto NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="410ce-104">NavigationCompletedEvent object</span></span>

<span data-ttu-id="410ce-105">Um objeto que representa um evento disparado quando o [WebView](../webview.md) concluiu o carregamento do conteúdo atual ou se houve falha na navegação.</span><span class="sxs-lookup"><span data-stu-id="410ce-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>

## <span data-ttu-id="410ce-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="410ce-106">Properties</span></span>
    
### <span data-ttu-id="410ce-107">uri</span><span class="sxs-lookup"><span data-stu-id="410ce-107">uri</span></span>

<span data-ttu-id="410ce-108">O URI (Uniform Resource Identifier) da navegação.</span><span class="sxs-lookup"><span data-stu-id="410ce-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>

<span data-ttu-id="410ce-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="410ce-109">This property is read-only.</span></span>

```js
var uri = NavigationCompletedEvent.uri;
```

#### <span data-ttu-id="410ce-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="410ce-110">Property value</span></span>
<span data-ttu-id="410ce-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="410ce-111">Type: **DOMString**</span></span>

### <span data-ttu-id="410ce-112">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="410ce-112">isSuccess</span></span>

<span data-ttu-id="410ce-113">Obtém um valor que indica se a navegação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="410ce-113">Gets a value that indicates whether the navigation completed successfully.</span></span>

<span data-ttu-id="410ce-114">Essa propriedade é somente leitura</span><span class="sxs-lookup"><span data-stu-id="410ce-114">This property is read-only</span></span>

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### <span data-ttu-id="410ce-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="410ce-115">Property value</span></span>
<span data-ttu-id="410ce-116">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="410ce-116">Type: **Boolean**</span></span>

### <span data-ttu-id="410ce-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="410ce-117">webErrorStatus</span></span>

<span data-ttu-id="410ce-118">Se a navegação não tiver sido bem-sucedida, obtém um valor que indica o motivo.</span><span class="sxs-lookup"><span data-stu-id="410ce-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>

<span data-ttu-id="410ce-119">Essa propriedade é somente leitura</span><span class="sxs-lookup"><span data-stu-id="410ce-119">This property is read-only</span></span>

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### <span data-ttu-id="410ce-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="410ce-120">Property value</span></span>
<span data-ttu-id="410ce-121">Tipo: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="410ce-121">Type: **unsigned long**</span></span>
