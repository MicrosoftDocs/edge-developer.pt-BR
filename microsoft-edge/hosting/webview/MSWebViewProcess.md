---
description: Representa um processo WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560968"
---
# <span data-ttu-id="cff2e-104">Objeto MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="cff2e-104">MSWebViewProcess object</span></span>

<span data-ttu-id="cff2e-105">Representa um processo [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="cff2e-105">Represents a [webview](../webview.md) process.</span></span>

```js
var wvprocess = new MSWebViewProcess();
```

## <span data-ttu-id="cff2e-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cff2e-106">Properties</span></span>

### <span data-ttu-id="cff2e-107">enterpriseid</span><span class="sxs-lookup"><span data-stu-id="cff2e-107">enterpriseId</span></span>

<span data-ttu-id="cff2e-108">A ID da empresa do processo.</span><span class="sxs-lookup"><span data-stu-id="cff2e-108">The enterprise ID of the process.</span></span>

```js
var enterpriseId = wvprocess.enterpriseId;
```

<span data-ttu-id="cff2e-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cff2e-109">This property is read-only.</span></span>

#### <span data-ttu-id="cff2e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cff2e-110">Property value</span></span>
<span data-ttu-id="cff2e-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="cff2e-111">Type: **DOMString**</span></span>

### <span data-ttu-id="cff2e-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="cff2e-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>

<span data-ttu-id="cff2e-113">Obtém um valor que indica se o processo [WebView](../webview.md) tem a [declaração de funcionalidade do aplicativo](/windows/uwp/packaging/app-capability-declarations) universal do Windows de *redes privadas (cliente & servidor)* habilitada no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cff2e-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

<span data-ttu-id="cff2e-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cff2e-114">This property is read-only.</span></span>

#### <span data-ttu-id="cff2e-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cff2e-115">Property value</span></span>
<span data-ttu-id="cff2e-116">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cff2e-116">Type: **Boolean**</span></span>

## <span data-ttu-id="cff2e-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="cff2e-117">Methods</span></span>

### <span data-ttu-id="cff2e-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="cff2e-118">CreateWebViewAsync</span></span>

<span data-ttu-id="cff2e-119">Cria uma [WebView](../webview.md) em um processo específico.</span><span class="sxs-lookup"><span data-stu-id="cff2e-119">Creates a [webview](../webview.md) in a specific process.</span></span>

```js
wvprocess.createWebviewAsync();
```

#### <span data-ttu-id="cff2e-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cff2e-120">Return value</span></span>

<span data-ttu-id="cff2e-121">Digite**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="cff2e-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="cff2e-122">Webviews</span><span class="sxs-lookup"><span data-stu-id="cff2e-122">GetWebViews</span></span>

<span data-ttu-id="cff2e-123">Retorna uma sequência de objetos **MSWebViewProcess** hospedados no processo.</span><span class="sxs-lookup"><span data-stu-id="cff2e-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>

#### <span data-ttu-id="cff2e-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cff2e-124">Return value</span></span>

<span data-ttu-id="cff2e-125">Digite**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="cff2e-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="cff2e-126">Inesperada</span><span class="sxs-lookup"><span data-stu-id="cff2e-126">Terminate</span></span>

<span data-ttu-id="cff2e-127">Finaliza o processo.</span><span class="sxs-lookup"><span data-stu-id="cff2e-127">Terminates the process.</span></span>

```js
wvprocess.terminate();
```

#### <span data-ttu-id="cff2e-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cff2e-128">Return value</span></span>

<span data-ttu-id="cff2e-129">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cff2e-129">This method does not return a value.</span></span>
