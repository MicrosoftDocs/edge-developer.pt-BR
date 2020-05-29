---
description: Expõe se a operação foi concluída com sucesso ou falhou
title: Objeto MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: ebb89c0fc645ebcd97357af10af2be650d8218b9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560969"
---
# <span data-ttu-id="3d953-104">Objeto MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="3d953-104">MSWebViewAsyncOperation object</span></span>

<span data-ttu-id="3d953-105">Expõe se a operação foi concluída com sucesso ou falhou.</span><span class="sxs-lookup"><span data-stu-id="3d953-105">Exposes whether the operation completed successfully or failed.</span></span> 

## <span data-ttu-id="3d953-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="3d953-106">Events</span></span>

### <span data-ttu-id="3d953-107">concluído</span><span class="sxs-lookup"><span data-stu-id="3d953-107">complete</span></span>

<span data-ttu-id="3d953-108">Indica que a operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="3d953-108">Indicates that the operation completed.</span></span> 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### <span data-ttu-id="3d953-109">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="3d953-109">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="3d953-110">Interface</span><span class="sxs-lookup"><span data-stu-id="3d953-110">Interface</span></span>** | **<span data-ttu-id="3d953-111">Evento</span><span class="sxs-lookup"><span data-stu-id="3d953-111">Event</span></span>**
|**<span data-ttu-id="3d953-112">Síncrono</span><span class="sxs-lookup"><span data-stu-id="3d953-112">Synchronous</span></span>** |<span data-ttu-id="3d953-113">Sim</span><span class="sxs-lookup"><span data-stu-id="3d953-113">Yes</span></span> |    
|**<span data-ttu-id="3d953-114">Bolhas</span><span class="sxs-lookup"><span data-stu-id="3d953-114">Bubbles</span></span>**     |<span data-ttu-id="3d953-115">Não</span><span class="sxs-lookup"><span data-stu-id="3d953-115">No</span></span> |   
|**<span data-ttu-id="3d953-116">Cela</span><span class="sxs-lookup"><span data-stu-id="3d953-116">Cancelable</span></span>**  |<span data-ttu-id="3d953-117">Não</span><span class="sxs-lookup"><span data-stu-id="3d953-117">No</span></span> |        


### <span data-ttu-id="3d953-118">erro</span><span class="sxs-lookup"><span data-stu-id="3d953-118">error</span></span>

<span data-ttu-id="3d953-119">Indica que houve um erro com a operação.</span><span class="sxs-lookup"><span data-stu-id="3d953-119">Indicates that there was an error with the operation.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### <span data-ttu-id="3d953-120">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="3d953-120">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="3d953-121">Interface</span><span class="sxs-lookup"><span data-stu-id="3d953-121">Interface</span></span>** | **<span data-ttu-id="3d953-122">Evento</span><span class="sxs-lookup"><span data-stu-id="3d953-122">Event</span></span>**
|**<span data-ttu-id="3d953-123">Síncrono</span><span class="sxs-lookup"><span data-stu-id="3d953-123">Synchronous</span></span>** |<span data-ttu-id="3d953-124">Sim</span><span class="sxs-lookup"><span data-stu-id="3d953-124">Yes</span></span> |    
|**<span data-ttu-id="3d953-125">Bolhas</span><span class="sxs-lookup"><span data-stu-id="3d953-125">Bubbles</span></span>**     |<span data-ttu-id="3d953-126">Não</span><span class="sxs-lookup"><span data-stu-id="3d953-126">No</span></span> |   
|**<span data-ttu-id="3d953-127">Cela</span><span class="sxs-lookup"><span data-stu-id="3d953-127">Cancelable</span></span>**  |<span data-ttu-id="3d953-128">Não</span><span class="sxs-lookup"><span data-stu-id="3d953-128">No</span></span> |            


## <span data-ttu-id="3d953-129">Métodos</span><span class="sxs-lookup"><span data-stu-id="3d953-129">Methods</span></span>

### <span data-ttu-id="3d953-130">start</span><span class="sxs-lookup"><span data-stu-id="3d953-130">start</span></span>

<span data-ttu-id="3d953-131">Chamado para iniciar a tarefa assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3d953-131">Called to start the async task.</span></span> 

```js
MSWebViewAsyncOperation.start();
```

### <span data-ttu-id="3d953-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d953-132">Parameters</span></span>

<span data-ttu-id="3d953-133">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3d953-133">This method does not have parameters.</span></span>

### <span data-ttu-id="3d953-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3d953-134">Return value</span></span>

<span data-ttu-id="3d953-135">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3d953-135">This method does not return a value.</span></span>

## <span data-ttu-id="3d953-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3d953-136">Properties</span></span>

### <span data-ttu-id="3d953-137">erro</span><span class="sxs-lookup"><span data-stu-id="3d953-137">error</span></span>

<span data-ttu-id="3d953-138">O erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="3d953-138">The error that occured.</span></span>

<span data-ttu-id="3d953-139">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d953-139">This property is read-only.</span></span>

```js
var error = MSWebViewAsyncOperation.error;
```

#### <span data-ttu-id="3d953-140">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d953-140">Property value</span></span>
<span data-ttu-id="3d953-141">Tipo: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="3d953-141">Type: **DOMError**</span></span>

### <span data-ttu-id="3d953-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="3d953-142">oncomplete</span></span>

<span data-ttu-id="3d953-143">O manipulador de eventos **completo** .</span><span class="sxs-lookup"><span data-stu-id="3d953-143">The **complete** event handler.</span></span> 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### <span data-ttu-id="3d953-144">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d953-144">Property value</span></span>
<span data-ttu-id="3d953-145">Tipo: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="3d953-145">Type: **EventHandler**</span></span>

### <span data-ttu-id="3d953-146">AoOcorrerErro</span><span class="sxs-lookup"><span data-stu-id="3d953-146">onerror</span></span>

<span data-ttu-id="3d953-147">O manipulador de eventos de **erro** .</span><span class="sxs-lookup"><span data-stu-id="3d953-147">The **error** event handler.</span></span> 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### <span data-ttu-id="3d953-148">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d953-148">Property value</span></span>
<span data-ttu-id="3d953-149">Tipo: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="3d953-149">Type: **EventHandler**</span></span>

### <span data-ttu-id="3d953-150">Ready</span><span class="sxs-lookup"><span data-stu-id="3d953-150">readyState</span></span>

<span data-ttu-id="3d953-151">Descreve o estado pronto do objeto.</span><span class="sxs-lookup"><span data-stu-id="3d953-151">Describes the ready state of the object.</span></span>

<span data-ttu-id="3d953-152">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d953-152">This property is read-only.</span></span>

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### <span data-ttu-id="3d953-153">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d953-153">Property value</span></span>
<span data-ttu-id="3d953-154">Tipo: **não assinado curto**</span><span class="sxs-lookup"><span data-stu-id="3d953-154">Type: **unsigned short**</span></span>

### <span data-ttu-id="3d953-155">levar</span><span class="sxs-lookup"><span data-stu-id="3d953-155">result</span></span>

<span data-ttu-id="3d953-156">O resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3d953-156">The result of the operation.</span></span>

<span data-ttu-id="3d953-157">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d953-157">This property is read-only.</span></span>

```js
var result = MSWebViewAsyncOperation.result;
```

#### <span data-ttu-id="3d953-158">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d953-158">Property value</span></span>
<span data-ttu-id="3d953-159">Tipo: qualquer</span><span class="sxs-lookup"><span data-stu-id="3d953-159">Type: any</span></span>

### <span data-ttu-id="3d953-160">target</span><span class="sxs-lookup"><span data-stu-id="3d953-160">target</span></span>

<span data-ttu-id="3d953-161">O destino da operação.</span><span class="sxs-lookup"><span data-stu-id="3d953-161">The target of the operation.</span></span> 

<span data-ttu-id="3d953-162">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d953-162">This property is read-only.</span></span>

```js
var target = MSWebViewAsyncOperation.target;
```

#### <span data-ttu-id="3d953-163">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d953-163">Property value</span></span>
<span data-ttu-id="3d953-164">Tipo: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="3d953-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>

### <span data-ttu-id="3d953-165">tipo</span><span class="sxs-lookup"><span data-stu-id="3d953-165">type</span></span>

<span data-ttu-id="3d953-166">O tipo da operação.</span><span class="sxs-lookup"><span data-stu-id="3d953-166">The type of the operation.</span></span>

<span data-ttu-id="3d953-167">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3d953-167">This property is read-only.</span></span>

```js
var type = MSWebViewAsyncOperation.type;
```

#### <span data-ttu-id="3d953-168">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3d953-168">Property value</span></span>
<span data-ttu-id="3d953-169">Tipo: **não assinado curto**</span><span class="sxs-lookup"><span data-stu-id="3d953-169">Type: **unsigned short**</span></span>
