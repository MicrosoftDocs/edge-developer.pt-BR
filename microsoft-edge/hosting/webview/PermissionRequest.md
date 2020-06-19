---
description: Fornece informações sobre uma solicitação de permissão
title: Objeto PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: c769bf122c3ca116d5783b73d0ff4f183d2cd52d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752112"
---
# <span data-ttu-id="7928f-104">Objeto PermissionRequest</span><span class="sxs-lookup"><span data-stu-id="7928f-104">PermissionRequest object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7928f-105">Fornece informações sobre uma solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="7928f-105">Provides information about a permission request.</span></span> <span data-ttu-id="7928f-106">Esse objeto está disponível na propriedade permissionRequest dos argumentos de evento do evento WebView [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) .</span><span class="sxs-lookup"><span data-stu-id="7928f-106">This object is available from the permissionRequest property of the event args from the [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) webview event.</span></span>  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});
```  

## <span data-ttu-id="7928f-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="7928f-107">Methods</span></span>  

### <span data-ttu-id="7928f-108">habilitar</span><span class="sxs-lookup"><span data-stu-id="7928f-108">allow</span></span>  

<span data-ttu-id="7928f-109">Permite a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="7928f-109">Allows the request for permission.</span></span>  

#### <span data-ttu-id="7928f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7928f-110">Parameters</span></span>  

<span data-ttu-id="7928f-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7928f-111">This method has no parameters.</span></span>  

#### <span data-ttu-id="7928f-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7928f-112">Return value</span></span>  

<span data-ttu-id="7928f-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7928f-113">This method does not return a value.</span></span>  

### <span data-ttu-id="7928f-114">adiar</span><span class="sxs-lookup"><span data-stu-id="7928f-114">defer</span></span>  

<span data-ttu-id="7928f-115">Se, em vez de, permitir ou não permitir ou não permitir uma PermissionRequest, você exigir um tempo para interagir com o usuário ou fazer outra ação assíncrona, a chamada adiará () no PermissionRequest.</span><span class="sxs-lookup"><span data-stu-id="7928f-115">If instead of synchronously allowing or disallowing a PermissionRequest, you require time to interact with the user or take some other asynchronous action, call defer() on the PermissionRequest.</span></span>  <span data-ttu-id="7928f-116">O PermissionRequest agora estará disponível como um DeferredPermissionRequest de getDeferredPermissionRequests e getDeferredPermissionRequestById.</span><span class="sxs-lookup"><span data-stu-id="7928f-116">The PermissionRequest will now be available as a DeferredPermissionRequest from getDeferredPermissionRequests and getDeferredPermissionRequestById.</span></span>  <span data-ttu-id="7928f-117">Você pode correlacionar o PermissionRequest atual com o DeferredPermissionRequest correspondente por meio da propriedade ID correspondente.</span><span class="sxs-lookup"><span data-stu-id="7928f-117">You can correlate the current PermissionRequest with the corresponding DeferredPermissionRequest via the matching id property.</span></span>  

#### <span data-ttu-id="7928f-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7928f-118">Parameters</span></span>  

<span data-ttu-id="7928f-119">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7928f-119">This method has no parameters.</span></span>  

#### <span data-ttu-id="7928f-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7928f-120">Return value</span></span>  

<span data-ttu-id="7928f-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7928f-121">This method does not return a value.</span></span>  

### <span data-ttu-id="7928f-122">negar</span><span class="sxs-lookup"><span data-stu-id="7928f-122">deny</span></span>  

<span data-ttu-id="7928f-123">Nega a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="7928f-123">Denies the request for permission.</span></span>  

#### <span data-ttu-id="7928f-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7928f-124">Parameters</span></span>  

<span data-ttu-id="7928f-125">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7928f-125">This method has no parameters.</span></span>  

#### <span data-ttu-id="7928f-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7928f-126">Return value</span></span>  

<span data-ttu-id="7928f-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7928f-127">This method does not return a value.</span></span>  

## <span data-ttu-id="7928f-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7928f-128">Properties</span></span>  

### <span data-ttu-id="7928f-129">id</span><span class="sxs-lookup"><span data-stu-id="7928f-129">id</span></span>  

<span data-ttu-id="7928f-130">Uma ID exclusiva que pode ser usada para correlacionar a PermissionRequest atual com um DeferredPermissionRequest correspondente se o método Defer for usado.</span><span class="sxs-lookup"><span data-stu-id="7928f-130">A unique ID that can be used to correlate the current PermissionRequest with a corresponding DeferredPermissionRequest if the defer method is used.</span></span>  <span data-ttu-id="7928f-131">Consulte o método Defer.</span><span class="sxs-lookup"><span data-stu-id="7928f-131">See the defer method.</span></span>  

<span data-ttu-id="7928f-132">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7928f-132">This property is read-only.</span></span>  

##### <span data-ttu-id="7928f-133">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7928f-133">Property value</span></span>  

<span data-ttu-id="7928f-134">Tipo: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="7928f-134">Type: **Unsigned long**</span></span>  

### <span data-ttu-id="7928f-135">Estado</span><span class="sxs-lookup"><span data-stu-id="7928f-135">state</span></span>  

<span data-ttu-id="7928f-136">Retorna "desconhecido", "adiar", "permitir" ou "negar" para indicar o estado atual de solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="7928f-136">Returns "unknown", "defer", "allow", or "deny" to indicate the current state of permission request.</span></span>  <span data-ttu-id="7928f-137">A cadeia de caracteres de estado corresponderá a qualquer método Allow, Deny ou Defer chamado Last ou "Unknown" se nenhum dos métodos tiver sido chamado.</span><span class="sxs-lookup"><span data-stu-id="7928f-137">The state string will correspond to whichever method allow, deny, or defer was called last or "unknown" if none of the methods have been called.</span></span>  

<span data-ttu-id="7928f-138">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7928f-138">This property is read-only.</span></span>  

#### <span data-ttu-id="7928f-139">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7928f-139">Property value</span></span>  

<span data-ttu-id="7928f-140">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7928f-140">Type: **String**</span></span>  

### <span data-ttu-id="7928f-141">tipo</span><span class="sxs-lookup"><span data-stu-id="7928f-141">type</span></span>  

<span data-ttu-id="7928f-142">O tipo de permissão que está sendo solicitada.</span><span class="sxs-lookup"><span data-stu-id="7928f-142">The type of permission being requested.</span></span> <span data-ttu-id="7928f-143">Pode ser um dos seguintes valores de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="7928f-143">This may be one of the following string values:</span></span>  

*   <span data-ttu-id="7928f-144">**geolocalização: acesso**a dados de localização via Navigator. geolocalização.</span><span class="sxs-lookup"><span data-stu-id="7928f-144">**geolocation**: access to location data via navigator.geolocation.</span></span>  
*   <span data-ttu-id="7928f-145">**unlimitedIndexedDBQuota**: permitir que as APIs do IndexedDB ignorem o limite de tamanho de dados armazenados usual.</span><span class="sxs-lookup"><span data-stu-id="7928f-145">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>  
*   <span data-ttu-id="7928f-146">**mídia**: acesso ao microfone e à câmera via Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="7928f-146">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>  
*   <span data-ttu-id="7928f-147">**pointerlock**: capacidade de bloquear e controlar o ponteiro do mouse via Element. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="7928f-147">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>  
*   <span data-ttu-id="7928f-148">**webnotifications**: capacidade de mostrar notificações da área de trabalho via janela. Forma.</span><span class="sxs-lookup"><span data-stu-id="7928f-148">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>  
*   <span data-ttu-id="7928f-149">**tela**: capacidade de fazer capturas de tela por meio da API de captura de mídia.</span><span class="sxs-lookup"><span data-stu-id="7928f-149">**screen**: ability to take screen shots via the Media Capture API.</span></span>  
*   <span data-ttu-id="7928f-150">**immersiveview**: capacidade de controlar uma exibição VR.</span><span class="sxs-lookup"><span data-stu-id="7928f-150">**immersiveview**: ability to control a VR display.</span></span>  

<span data-ttu-id="7928f-151">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7928f-151">This property is read-only.</span></span>  

#### <span data-ttu-id="7928f-152">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7928f-152">Property value</span></span>  

<span data-ttu-id="7928f-153">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7928f-153">Type: **String**</span></span>  

### <span data-ttu-id="7928f-154">uri</span><span class="sxs-lookup"><span data-stu-id="7928f-154">uri</span></span>  

<span data-ttu-id="7928f-155">O URI (Uniform Resource Identifier) do documento que solicita permissão.</span><span class="sxs-lookup"><span data-stu-id="7928f-155">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>  

<span data-ttu-id="7928f-156">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7928f-156">This property is read-only.</span></span>  

#### <span data-ttu-id="7928f-157">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7928f-157">Property value</span></span>  

<span data-ttu-id="7928f-158">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7928f-158">Type: **String**</span></span>  
