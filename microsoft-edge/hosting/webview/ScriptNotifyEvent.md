---
description: Representa uma cadeia de caracteres de notificação passada do conteúdo WebView para o aplicativo
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10560492"
---
# <span data-ttu-id="d0039-104">Objeto ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="d0039-104">ScriptNotifyEvent object</span></span>

<span data-ttu-id="d0039-105">Um objeto que representa um evento disparado quando o conteúdo contido no [WebView](../webview.md) passa uma cadeia de caracteres para o aplicativo usando JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d0039-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>

## <span data-ttu-id="d0039-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d0039-106">Properties</span></span>
    
### <span data-ttu-id="d0039-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="d0039-107">callingUri</span></span>

<span data-ttu-id="d0039-108">Obtém o URI (Uniform Resource Identifier) da página que contém o script que disparou o **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="d0039-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>

<span data-ttu-id="d0039-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d0039-109">This property is read-only.</span></span>

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### <span data-ttu-id="d0039-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d0039-110">Property value</span></span>
<span data-ttu-id="d0039-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="d0039-111">Type: **DOMString**</span></span>

### <span data-ttu-id="d0039-112">value</span><span class="sxs-lookup"><span data-stu-id="d0039-112">value</span></span>

<span data-ttu-id="d0039-113">O nome do método como passado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0039-113">The method name as passed to the application.</span></span>

<span data-ttu-id="d0039-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d0039-114">This property is read-only.</span></span>

```js
var value = ScriptNotifyEvent.value;
```

#### <span data-ttu-id="d0039-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d0039-115">Property value</span></span>
<span data-ttu-id="d0039-116">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="d0039-116">Type: **DOMString**</span></span>