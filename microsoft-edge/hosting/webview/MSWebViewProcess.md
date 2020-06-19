---
description: Representa um processo WebView.
title: Objeto MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752149"
---
# <span data-ttu-id="52455-104">Objeto MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="52455-104">MSWebViewProcess object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="52455-105">Representa um processo [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="52455-105">Represents a [webview](../webview.md) process.</span></span>  

```javascript
var wvprocess = new MSWebViewProcess();
```  

## <span data-ttu-id="52455-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52455-106">Properties</span></span>  

### <span data-ttu-id="52455-107">enterpriseid</span><span class="sxs-lookup"><span data-stu-id="52455-107">enterpriseId</span></span>  

<span data-ttu-id="52455-108">A ID da empresa do processo.</span><span class="sxs-lookup"><span data-stu-id="52455-108">The enterprise ID of the process.</span></span>  

```js
var enterpriseId = wvprocess.enterpriseId;
```  

<span data-ttu-id="52455-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="52455-109">This property is read-only.</span></span>  

#### <span data-ttu-id="52455-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52455-110">Property value</span></span>  

<span data-ttu-id="52455-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="52455-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="52455-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="52455-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>  

<span data-ttu-id="52455-113">Obtém um valor que indica se o processo [WebView](../webview.md) tem a [declaração de funcionalidade do aplicativo](/windows/uwp/packaging/app-capability-declarations) universal do Windows de *redes privadas (cliente & servidor)* habilitada no manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="52455-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>  

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

<span data-ttu-id="52455-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="52455-114">This property is read-only.</span></span>  

#### <span data-ttu-id="52455-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52455-115">Property value</span></span>  

<span data-ttu-id="52455-116">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="52455-116">Type: **Boolean**</span></span>  

## <span data-ttu-id="52455-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="52455-117">Methods</span></span>  

### <span data-ttu-id="52455-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="52455-118">CreateWebViewAsync</span></span>  

<span data-ttu-id="52455-119">Cria uma [WebView](../webview.md) em um processo específico.</span><span class="sxs-lookup"><span data-stu-id="52455-119">Creates a [webview](../webview.md) in a specific process.</span></span>  

```javascript
wvprocess.createWebviewAsync();
```  

#### <span data-ttu-id="52455-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="52455-120">Return value</span></span>  

<span data-ttu-id="52455-121">Digite**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="52455-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="52455-122">Webviews</span><span class="sxs-lookup"><span data-stu-id="52455-122">GetWebViews</span></span>  

<span data-ttu-id="52455-123">Retorna uma sequência de objetos **MSWebViewProcess** hospedados no processo.</span><span class="sxs-lookup"><span data-stu-id="52455-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>  

#### <span data-ttu-id="52455-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="52455-124">Return value</span></span>  

<span data-ttu-id="52455-125">Digite**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="52455-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="52455-126">Inesperada</span><span class="sxs-lookup"><span data-stu-id="52455-126">Terminate</span></span>  

<span data-ttu-id="52455-127">Finaliza o processo.</span><span class="sxs-lookup"><span data-stu-id="52455-127">Terminates the process.</span></span>  

```javascript
wvprocess.terminate();
```  

#### <span data-ttu-id="52455-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="52455-128">Return value</span></span>  

<span data-ttu-id="52455-129">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="52455-129">This method does not return a value.</span></span>  
