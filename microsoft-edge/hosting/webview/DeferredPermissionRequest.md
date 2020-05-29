---
description: Representa uma solicitação adiada para a permissão do usuário acessar a funcionalidade do dispositivo
title: Objeto DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 6013f20195fc0f5d4f33b871a9c1b01392bf023e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560978"
---
# <span data-ttu-id="4435b-104">Objeto DeferredPermissionRequest</span><span class="sxs-lookup"><span data-stu-id="4435b-104">DeferredPermissionRequest object</span></span>

<span data-ttu-id="4435b-105">Representa uma solicitação adiada pelo conteúdo da [WebView](../webview.md) para permissão de usuário final para acessar funcionalidade de dispositivo especializada (como geolocalização ou bloqueio de ponteiro).</span><span class="sxs-lookup"><span data-stu-id="4435b-105">Represents a deferred request by the content of the [webview](../webview.md) for end-user permission to access specialized device functionality (such as geolocation, or pointer lock).</span></span>

```js
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```

## <span data-ttu-id="4435b-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="4435b-106">Methods</span></span>

### <span data-ttu-id="4435b-107">habilitar</span><span class="sxs-lookup"><span data-stu-id="4435b-107">allow</span></span>

<span data-ttu-id="4435b-108">Permite a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="4435b-108">Allows the request for permission.</span></span>

```js
deferredPermissionRequest.allow();
```

#### <span data-ttu-id="4435b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4435b-109">Parameters</span></span>

<span data-ttu-id="4435b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4435b-110">This method has no parameters.</span></span>

#### <span data-ttu-id="4435b-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4435b-111">Return value</span></span>

<span data-ttu-id="4435b-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4435b-112">This method does not return a value.</span></span>

### <span data-ttu-id="4435b-113">negar</span><span class="sxs-lookup"><span data-stu-id="4435b-113">deny</span></span>

<span data-ttu-id="4435b-114">Nega a solicitação de permissão.</span><span class="sxs-lookup"><span data-stu-id="4435b-114">Denies the request for permission.</span></span>

```js
deferredPermissionRequest.deny();
```

#### <span data-ttu-id="4435b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4435b-115">Parameters</span></span>

<span data-ttu-id="4435b-116">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4435b-116">This method has no parameters.</span></span>

#### <span data-ttu-id="4435b-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4435b-117">Return value</span></span>

<span data-ttu-id="4435b-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4435b-118">This method does not return a value.</span></span>

## <span data-ttu-id="4435b-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4435b-119">Properties</span></span>

### <span data-ttu-id="4435b-120">id</span><span class="sxs-lookup"><span data-stu-id="4435b-120">id</span></span>

<span data-ttu-id="4435b-121">Uma ID exclusiva que pode ser usada para correlacionar a DeferredPermissionRequest atual com um objeto PermissionRequest de um evento MSWebViewPermissionRequested anterior.</span><span class="sxs-lookup"><span data-stu-id="4435b-121">A unique ID that can be used to correlate the current DeferredPermissionRequest with a PermissionRequest object from a previous MSWebViewPermissionRequested event.</span></span> <span data-ttu-id="4435b-122">Consulte o método **PermissionRequested. Defer** .</span><span class="sxs-lookup"><span data-stu-id="4435b-122">See the **PermissionRequested.defer** method.</span></span>

<span data-ttu-id="4435b-123">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4435b-123">This property is read-only.</span></span>

```js
var id = deferredPermissionRequest.id;
```

##### <span data-ttu-id="4435b-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4435b-124">Property value</span></span>

<span data-ttu-id="4435b-125">Tipo: **unsigned long**</span><span class="sxs-lookup"><span data-stu-id="4435b-125">Type: **Unsigned long**</span></span>

### <span data-ttu-id="4435b-126">tipo</span><span class="sxs-lookup"><span data-stu-id="4435b-126">type</span></span>

<span data-ttu-id="4435b-127">O tipo de permissão que está sendo solicitada.</span><span class="sxs-lookup"><span data-stu-id="4435b-127">The type of permission being requested.</span></span> <span data-ttu-id="4435b-128">Pode ser um dos seguintes valores de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="4435b-128">This may be one of the following string values:</span></span>

- <span data-ttu-id="4435b-129">**geolocalização: acesso**a dados de localização via Navigator. geolocalização.</span><span class="sxs-lookup"><span data-stu-id="4435b-129">**geolocation**: access to location data via navigator.geolocation.</span></span>
- <span data-ttu-id="4435b-130">**unlimitedIndexedDBQuota**: permitir que as APIs do IndexedDB ignorem o limite de tamanho de dados armazenados usual.</span><span class="sxs-lookup"><span data-stu-id="4435b-130">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>
- <span data-ttu-id="4435b-131">**mídia**: acesso ao microfone e à câmera via Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="4435b-131">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>
- <span data-ttu-id="4435b-132">**pointerlock**: capacidade de bloquear e controlar o ponteiro do mouse via Element. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="4435b-132">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>
- <span data-ttu-id="4435b-133">**webnotifications**: capacidade de mostrar notificações da área de trabalho via janela. Forma.</span><span class="sxs-lookup"><span data-stu-id="4435b-133">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>
- <span data-ttu-id="4435b-134">**tela**: capacidade de fazer capturas de tela por meio da API de captura de mídia.</span><span class="sxs-lookup"><span data-stu-id="4435b-134">**screen**: ability to take screen shots via the Media Capture API.</span></span>
- <span data-ttu-id="4435b-135">**immersiveview**: capacidade de controlar uma exibição VR.</span><span class="sxs-lookup"><span data-stu-id="4435b-135">**immersiveview**: ability to control a VR display.</span></span>

<span data-ttu-id="4435b-136">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4435b-136">This property is read-only.</span></span>

```js
var type = deferredPermissionRequest.type;
```

#### <span data-ttu-id="4435b-137">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4435b-137">Property value</span></span>

<span data-ttu-id="4435b-138">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4435b-138">Type: **String**</span></span>

### <span data-ttu-id="4435b-139">uri</span><span class="sxs-lookup"><span data-stu-id="4435b-139">uri</span></span>

<span data-ttu-id="4435b-140">O URI (Uniform Resource Identifier) do documento que solicita permissão.</span><span class="sxs-lookup"><span data-stu-id="4435b-140">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>

<span data-ttu-id="4435b-141">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="4435b-141">This property is read-only.</span></span>

```js
var uri = deferredPermissionRequest.uri;
```

##### <span data-ttu-id="4435b-142">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4435b-142">Property value</span></span>

<span data-ttu-id="4435b-143">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4435b-143">Type: **String**</span></span>

## <span data-ttu-id="4435b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4435b-144">Requirements</span></span>

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong><span data-ttu-id="4435b-145">Mínimo de cliente com suporte</span><span class="sxs-lookup"><span data-stu-id="4435b-145">Minimum supported client</span></span></strong> | <span data-ttu-id="4435b-146">Windows 10 [somente aplicativos da Windows Store]</span><span class="sxs-lookup"><span data-stu-id="4435b-146">Windows 10 [Windows Store apps only]</span></span> |
| <strong><span data-ttu-id="4435b-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4435b-147">Minimum supported server</span></span></strong> |            <span data-ttu-id="4435b-148">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4435b-148">Not supported</span></span>             |
| <strong><span data-ttu-id="4435b-149">Número mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4435b-149">Minimum supported phone</span></span></strong>  |            <span data-ttu-id="4435b-150">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4435b-150">Not supported</span></span>             |
