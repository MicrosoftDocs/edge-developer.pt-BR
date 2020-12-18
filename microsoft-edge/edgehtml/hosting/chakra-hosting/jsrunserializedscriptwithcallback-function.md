---
description: Executa um script serializado. Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.
title: Função JsRunSerializedScriptWithCallback | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ac9ac08357cd479f78e3500bc5eef151fb8e4e6c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231918"
---
# <span data-ttu-id="b63f1-104">Função JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="b63f1-104">JsRunSerializedScriptWithCallback Function</span></span>

<span data-ttu-id="b63f1-105">Executa um script serializado.</span><span class="sxs-lookup"><span data-stu-id="b63f1-105">Runs a serialized script.</span></span> <span data-ttu-id="b63f1-106">Fornece a capacidade de carregar a fonte de script somente se/quando for necessária.</span><span class="sxs-lookup"><span data-stu-id="b63f1-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="b63f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b63f1-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="b63f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b63f1-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="b63f1-109">Retorno de chamada chamado quando o código-fonte do script precisa ser carregado.</span><span class="sxs-lookup"><span data-stu-id="b63f1-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="b63f1-110">Retorno de chamada chamado quando o script serializado e o código-fonte não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="b63f1-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="b63f1-111">O script serializado.</span><span class="sxs-lookup"><span data-stu-id="b63f1-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="b63f1-112">Um cookie identificando o script que pode ser usado por contextos de script debuggable.</span><span class="sxs-lookup"><span data-stu-id="b63f1-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="b63f1-113">Esse contexto passará para scriptLoadCallback e scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="b63f1-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="b63f1-114">O local de onde o script veio.</span><span class="sxs-lookup"><span data-stu-id="b63f1-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="b63f1-115">O resultado da execução do script, se houver.</span><span class="sxs-lookup"><span data-stu-id="b63f1-115">The result of running the script, if any.</span></span> <span data-ttu-id="b63f1-116">Esse parâmetro pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="b63f1-116">This parameter can be null.</span></span>  
  
## <span data-ttu-id="b63f1-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b63f1-117">Return Value</span></span>  
 <span data-ttu-id="b63f1-118">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="b63f1-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b63f1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b63f1-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b63f1-120">Esta API ainda não está disponível para aplicativos da loja.</span><span class="sxs-lookup"><span data-stu-id="b63f1-120">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="b63f1-121">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="b63f1-121">Requires an active script context.</span></span>  
  
 <span data-ttu-id="b63f1-122">O tempo de execução será armazenado no buffer até que todas as instâncias criadas do buffer sejam coletadas como lixo.</span><span class="sxs-lookup"><span data-stu-id="b63f1-122">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="b63f1-123">Em seguida, ele chamará scriptUnloadCallback para informar ao chamador que é seguro liberar.</span><span class="sxs-lookup"><span data-stu-id="b63f1-123">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="b63f1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b63f1-124">Requirements</span></span>  
 <span data-ttu-id="b63f1-125">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b63f1-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b63f1-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b63f1-126">See Also</span></span>  
 [<span data-ttu-id="b63f1-127">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b63f1-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
