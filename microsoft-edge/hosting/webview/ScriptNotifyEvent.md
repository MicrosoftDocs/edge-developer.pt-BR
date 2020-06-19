---
description: Representa uma cadeia de caracteres de notificação passada do conteúdo WebView para o aplicativo
title: Objeto ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752007"
---
# <span data-ttu-id="5ab2b-104">Objeto ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="5ab2b-104">ScriptNotifyEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="5ab2b-105">Um objeto que representa um evento disparado quando o conteúdo contido no [WebView](../webview.md) passa uma cadeia de caracteres para o aplicativo usando JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5ab2b-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>  

## <span data-ttu-id="5ab2b-106">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ab2b-106">Properties</span></span>  

### <span data-ttu-id="5ab2b-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="5ab2b-107">callingUri</span></span>  

<span data-ttu-id="5ab2b-108">Obtém o URI (Uniform Resource Identifier) da página que contém o script que disparou o **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="5ab2b-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>  

<span data-ttu-id="5ab2b-109">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5ab2b-109">This property is read-only.</span></span>  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### <span data-ttu-id="5ab2b-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5ab2b-110">Property value</span></span>  

<span data-ttu-id="5ab2b-111">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="5ab2b-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="5ab2b-112">value</span><span class="sxs-lookup"><span data-stu-id="5ab2b-112">value</span></span>  

<span data-ttu-id="5ab2b-113">O nome do método como passado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ab2b-113">The method name as passed to the application.</span></span>  

<span data-ttu-id="5ab2b-114">Essa propriedade é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5ab2b-114">This property is read-only.</span></span>  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### <span data-ttu-id="5ab2b-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5ab2b-115">Property value</span></span>  

<span data-ttu-id="5ab2b-116">Tipo: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="5ab2b-116">Type: **DOMString**</span></span>  
