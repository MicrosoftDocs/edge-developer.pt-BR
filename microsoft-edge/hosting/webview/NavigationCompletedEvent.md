---
description: Contém informações sobre a navegação da WebView completada
title: Objeto NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752133"
---
# <span data-ttu-id="6e3a2-104">Objeto NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="6e3a2-104">NavigationCompletedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="6e3a2-105">Um objeto que representa um evento disparado quando o [WebView](../webview.md) concluiu o carregamento do conteúdo atual ou se houve falha na navegação.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>  

## <span data-ttu-id="6e3a2-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6e3a2-106">Properties</span></span>  

### <span data-ttu-id="6e3a2-107">uri</span><span class="sxs-lookup"><span data-stu-id="6e3a2-107">uri</span></span>  

<span data-ttu-id="6e3a2-108">O URI (Uniform Resource Identifier) da navegação.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>  

<span data-ttu-id="6e3a2-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-109">This property is read-only.</span></span>  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### <span data-ttu-id="6e3a2-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e3a2-110">Property value</span></span>  

<span data-ttu-id="6e3a2-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="6e3a2-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="6e3a2-112">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="6e3a2-112">isSuccess</span></span>  

<span data-ttu-id="6e3a2-113">Obtém um valor que indica se a navegação foi concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-113">Gets a value that indicates whether the navigation completed successfully.</span></span>  

<span data-ttu-id="6e3a2-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-114">This property is read-only.</span></span>  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### <span data-ttu-id="6e3a2-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e3a2-115">Property value</span></span>  

<span data-ttu-id="6e3a2-116">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6e3a2-116">Type: **Boolean**</span></span>  

### <span data-ttu-id="6e3a2-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="6e3a2-117">webErrorStatus</span></span>  

<span data-ttu-id="6e3a2-118">Se a navegação não tiver sido bem-sucedida, obtém um valor que indica o motivo.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>  

<span data-ttu-id="6e3a2-119">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="6e3a2-119">This property is read-only.</span></span>  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### <span data-ttu-id="6e3a2-120">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6e3a2-120">Property value</span></span>  

<span data-ttu-id="6e3a2-121">Tipo: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="6e3a2-121">Type: **unsigned long**</span></span>  
