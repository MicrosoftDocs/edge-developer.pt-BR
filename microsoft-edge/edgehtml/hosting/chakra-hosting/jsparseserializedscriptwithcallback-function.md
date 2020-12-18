---
description: Analisa um script serializado e retorna uma função que representa o script. Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.
title: Função JsParseSerializedScriptWithCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b145f01a5c3459100d8402beae63b7cff55db7b8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231750"
---
# <span data-ttu-id="a01ec-104">Função JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="a01ec-104">JsParseSerializedScriptWithCallback Function</span></span>

<span data-ttu-id="a01ec-105">Analisa um script serializado e retorna uma função que representa o script.</span><span class="sxs-lookup"><span data-stu-id="a01ec-105">Parses a serialized script and returns a function representing the script.</span></span> <span data-ttu-id="a01ec-106">Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.</span><span class="sxs-lookup"><span data-stu-id="a01ec-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="a01ec-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a01ec-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### <span data-ttu-id="a01ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a01ec-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="a01ec-109">Retorno de chamada chamado quando o código-fonte do script precisa ser carregado.</span><span class="sxs-lookup"><span data-stu-id="a01ec-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="a01ec-110">Retorno de chamada chamado quando o script serializado e o código-fonte não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="a01ec-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="a01ec-111">O script serializado.</span><span class="sxs-lookup"><span data-stu-id="a01ec-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="a01ec-112">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="a01ec-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="a01ec-113">Esse contexto passará para scriptLoadCallback e scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="a01ec-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="a01ec-114">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="a01ec-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="a01ec-115">Uma função que representa o código de script.</span><span class="sxs-lookup"><span data-stu-id="a01ec-115">A function representing the script code.</span></span>  
  
## <span data-ttu-id="a01ec-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a01ec-116">Return Value</span></span>  
 <span data-ttu-id="a01ec-117">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="a01ec-117">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a01ec-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a01ec-118">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a01ec-119">Esta API ainda não está disponível para aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="a01ec-119">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="a01ec-120">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="a01ec-120">Requires an active script context.</span></span>  
  
 <span data-ttu-id="a01ec-121">O tempo de execução será armazenado no buffer até que todas as instâncias criadas do buffer sejam coletadas como lixo.</span><span class="sxs-lookup"><span data-stu-id="a01ec-121">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="a01ec-122">Em seguida, ele chamará scriptUnloadCallback para informar ao chamador que é seguro liberar.</span><span class="sxs-lookup"><span data-stu-id="a01ec-122">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="a01ec-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a01ec-123">Requirements</span></span>  
 <span data-ttu-id="a01ec-124">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a01ec-124">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a01ec-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a01ec-125">See Also</span></span>  
 [<span data-ttu-id="a01ec-126">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a01ec-126">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
