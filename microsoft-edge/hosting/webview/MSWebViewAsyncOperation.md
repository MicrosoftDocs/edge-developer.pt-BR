---
description: Expõe se a operação foi concluída com sucesso ou falhou
title: Objeto MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: d6e03af2a0205938f19120076aa0ad622539d7e5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752119"
---
# <span data-ttu-id="7302f-104">Objeto MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="7302f-104">MSWebViewAsyncOperation object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7302f-105">Expõe se a operação foi concluída com sucesso ou falhou.</span><span class="sxs-lookup"><span data-stu-id="7302f-105">Exposes whether the operation completed successfully or failed.</span></span>  

## <span data-ttu-id="7302f-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="7302f-106">Events</span></span>  

### <span data-ttu-id="7302f-107">concluído</span><span class="sxs-lookup"><span data-stu-id="7302f-107">complete</span></span>  

<span data-ttu-id="7302f-108">Indica que a operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7302f-108">Indicates that the operation completed.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### <span data-ttu-id="7302f-109">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="7302f-109">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="7302f-110">Interface</span><span class="sxs-lookup"><span data-stu-id="7302f-110">Interface</span></span>** | **<span data-ttu-id="7302f-111">Evento</span><span class="sxs-lookup"><span data-stu-id="7302f-111">Event</span></span>** |  
| **<span data-ttu-id="7302f-112">Síncrono</span><span class="sxs-lookup"><span data-stu-id="7302f-112">Synchronous</span></span>** |<span data-ttu-id="7302f-113">Sim</span><span class="sxs-lookup"><span data-stu-id="7302f-113">Yes</span></span> |  
| **<span data-ttu-id="7302f-114">Bolhas</span><span class="sxs-lookup"><span data-stu-id="7302f-114">Bubbles</span></span>** |<span data-ttu-id="7302f-115">Não</span><span class="sxs-lookup"><span data-stu-id="7302f-115">No</span></span> |   
| **<span data-ttu-id="7302f-116">Cela</span><span class="sxs-lookup"><span data-stu-id="7302f-116">Cancelable</span></span>** |<span data-ttu-id="7302f-117">Não</span><span class="sxs-lookup"><span data-stu-id="7302f-117">No</span></span> |  

### <span data-ttu-id="7302f-118">erro</span><span class="sxs-lookup"><span data-stu-id="7302f-118">error</span></span>  

<span data-ttu-id="7302f-119">Indica que houve um erro com a operação.</span><span class="sxs-lookup"><span data-stu-id="7302f-119">Indicates that there was an error with the operation.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### <span data-ttu-id="7302f-120">Informações do evento</span><span class="sxs-lookup"><span data-stu-id="7302f-120">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="7302f-121">Interface</span><span class="sxs-lookup"><span data-stu-id="7302f-121">Interface</span></span>** | **<span data-ttu-id="7302f-122">Evento</span><span class="sxs-lookup"><span data-stu-id="7302f-122">Event</span></span>** |  
| **<span data-ttu-id="7302f-123">Síncrono</span><span class="sxs-lookup"><span data-stu-id="7302f-123">Synchronous</span></span>** | <span data-ttu-id="7302f-124">Sim</span><span class="sxs-lookup"><span data-stu-id="7302f-124">Yes</span></span> |  
| **<span data-ttu-id="7302f-125">Bolhas</span><span class="sxs-lookup"><span data-stu-id="7302f-125">Bubbles</span></span>** | <span data-ttu-id="7302f-126">Não</span><span class="sxs-lookup"><span data-stu-id="7302f-126">No</span></span> |  
| **<span data-ttu-id="7302f-127">Cela</span><span class="sxs-lookup"><span data-stu-id="7302f-127">Cancelable</span></span>** | <span data-ttu-id="7302f-128">Não</span><span class="sxs-lookup"><span data-stu-id="7302f-128">No</span></span> |  

## <span data-ttu-id="7302f-129">Métodos</span><span class="sxs-lookup"><span data-stu-id="7302f-129">Methods</span></span>  

### <span data-ttu-id="7302f-130">start</span><span class="sxs-lookup"><span data-stu-id="7302f-130">start</span></span>  

<span data-ttu-id="7302f-131">Chamado para iniciar a tarefa assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7302f-131">Called to start the async task.</span></span>  

```javascript
MSWebViewAsyncOperation.start();
```  

### <span data-ttu-id="7302f-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7302f-132">Parameters</span></span>  

<span data-ttu-id="7302f-133">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7302f-133">This method does not have parameters.</span></span>  

### <span data-ttu-id="7302f-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7302f-134">Return value</span></span>  

<span data-ttu-id="7302f-135">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7302f-135">This method does not return a value.</span></span>  

## <span data-ttu-id="7302f-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7302f-136">Properties</span></span>  

### <span data-ttu-id="7302f-137">erro</span><span class="sxs-lookup"><span data-stu-id="7302f-137">error</span></span>  

<span data-ttu-id="7302f-138">O erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="7302f-138">The error that occurred.</span></span>  

<span data-ttu-id="7302f-139">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7302f-139">This property is read-only.</span></span>  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### <span data-ttu-id="7302f-140">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7302f-140">Property value</span></span>  

<span data-ttu-id="7302f-141">Tipo: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="7302f-141">Type: **DOMError**</span></span>  

### <span data-ttu-id="7302f-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="7302f-142">oncomplete</span></span>  

<span data-ttu-id="7302f-143">O manipulador de eventos **completo** .</span><span class="sxs-lookup"><span data-stu-id="7302f-143">The **complete** event handler.</span></span>  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### <span data-ttu-id="7302f-144">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7302f-144">Property value</span></span>  

<span data-ttu-id="7302f-145">Tipo: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="7302f-145">Type: **EventHandler**</span></span>  

### <span data-ttu-id="7302f-146">AoOcorrerErro</span><span class="sxs-lookup"><span data-stu-id="7302f-146">onerror</span></span>  

<span data-ttu-id="7302f-147">O manipulador de eventos de **erro** .</span><span class="sxs-lookup"><span data-stu-id="7302f-147">The **error** event handler.</span></span>  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### <span data-ttu-id="7302f-148">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7302f-148">Property value</span></span>  

<span data-ttu-id="7302f-149">Tipo: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="7302f-149">Type: **EventHandler**</span></span>  

### <span data-ttu-id="7302f-150">Ready</span><span class="sxs-lookup"><span data-stu-id="7302f-150">readyState</span></span>  

<span data-ttu-id="7302f-151">Descreve o estado pronto do objeto.</span><span class="sxs-lookup"><span data-stu-id="7302f-151">Describes the ready state of the object.</span></span>  

<span data-ttu-id="7302f-152">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7302f-152">This property is read-only.</span></span>  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### <span data-ttu-id="7302f-153">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7302f-153">Property value</span></span>  

<span data-ttu-id="7302f-154">Tipo: **não assinado curto**</span><span class="sxs-lookup"><span data-stu-id="7302f-154">Type: **unsigned short**</span></span>  

### <span data-ttu-id="7302f-155">levar</span><span class="sxs-lookup"><span data-stu-id="7302f-155">result</span></span>  

<span data-ttu-id="7302f-156">O resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="7302f-156">The result of the operation.</span></span>  

<span data-ttu-id="7302f-157">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7302f-157">This property is read-only.</span></span>  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### <span data-ttu-id="7302f-158">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7302f-158">Property value</span></span>  

<span data-ttu-id="7302f-159">Tipo: qualquer</span><span class="sxs-lookup"><span data-stu-id="7302f-159">Type: any</span></span>  

### <span data-ttu-id="7302f-160">target</span><span class="sxs-lookup"><span data-stu-id="7302f-160">target</span></span>  

<span data-ttu-id="7302f-161">O destino da operação.</span><span class="sxs-lookup"><span data-stu-id="7302f-161">The target of the operation.</span></span>  

<span data-ttu-id="7302f-162">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7302f-162">This property is read-only.</span></span>  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### <span data-ttu-id="7302f-163">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7302f-163">Property value</span></span>  

<span data-ttu-id="7302f-164">Tipo: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="7302f-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>  

### <span data-ttu-id="7302f-165">tipo</span><span class="sxs-lookup"><span data-stu-id="7302f-165">type</span></span>  

<span data-ttu-id="7302f-166">O tipo da operação.</span><span class="sxs-lookup"><span data-stu-id="7302f-166">The type of the operation.</span></span>  

<span data-ttu-id="7302f-167">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7302f-167">This property is read-only.</span></span>  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### <span data-ttu-id="7302f-168">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7302f-168">Property value</span></span>  

<span data-ttu-id="7302f-169">Tipo: **não assinado curto**</span><span class="sxs-lookup"><span data-stu-id="7302f-169">Type: **unsigned short**</span></span>  
