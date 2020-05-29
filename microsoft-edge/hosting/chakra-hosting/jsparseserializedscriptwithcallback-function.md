---
description: Analisa um script serializado e retorna uma função que representa o script. Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.
title: Função JsParseSerializedScriptWithCallback | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ad6d635722f0b3fea8b19f8d16679b402d1fd56e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562146"
---
# <span data-ttu-id="201a4-104">Função JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="201a4-104">JsParseSerializedScriptWithCallback Function</span></span>
<span data-ttu-id="201a4-105">Analisa um script serializado e retorna uma função que representa o script.</span><span class="sxs-lookup"><span data-stu-id="201a4-105">Parses a serialized script and returns a function representing the script.</span></span> <span data-ttu-id="201a4-106">Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.</span><span class="sxs-lookup"><span data-stu-id="201a4-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="201a4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="201a4-107">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="201a4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="201a4-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="201a4-109">Retorno de chamada chamado quando o código-fonte do script precisa ser carregado.</span><span class="sxs-lookup"><span data-stu-id="201a4-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="201a4-110">Retorno de chamada chamado quando o script serializado e o código-fonte não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="201a4-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="201a4-111">O script serializado.</span><span class="sxs-lookup"><span data-stu-id="201a4-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="201a4-112">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="201a4-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="201a4-113">Esse contexto passará para scriptLoadCallback e scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="201a4-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="201a4-114">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="201a4-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="201a4-115">Uma função que representa o código de script.</span><span class="sxs-lookup"><span data-stu-id="201a4-115">A function representing the script code.</span></span>  
  
## <span data-ttu-id="201a4-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="201a4-116">Return Value</span></span>  
 <span data-ttu-id="201a4-117">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="201a4-117">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="201a4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="201a4-118">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="201a4-119">Esta API ainda não está disponível para aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="201a4-119">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="201a4-120">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="201a4-120">Requires an active script context.</span></span>  
  
 <span data-ttu-id="201a4-121">O tempo de execução será armazenado no buffer até que todas as instâncias criadas do buffer sejam coletadas como lixo.</span><span class="sxs-lookup"><span data-stu-id="201a4-121">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="201a4-122">Em seguida, ele chamará scriptUnloadCallback para informar ao chamador que é seguro liberar.</span><span class="sxs-lookup"><span data-stu-id="201a4-122">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="201a4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="201a4-123">Requirements</span></span>  
 <span data-ttu-id="201a4-124">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="201a4-124">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="201a4-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="201a4-125">See Also</span></span>  
 [<span data-ttu-id="201a4-126">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="201a4-126">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)