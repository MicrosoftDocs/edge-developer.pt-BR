---
description: Cria um `ArrayBuffer` objeto JavaScript para acessar a memória externa.
title: Função JsCreateExternalArrayBuffer | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 78c0d3c8b298876358f247c86a488b6f10e52c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231813"
---
# <span data-ttu-id="ddad6-103">Função JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="ddad6-103">JsCreateExternalArrayBuffer Function</span></span>

<span data-ttu-id="ddad6-104">Cria um `ArrayBuffer` objeto JavaScript para acessar a memória externa.</span><span class="sxs-lookup"><span data-stu-id="ddad6-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="ddad6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ddad6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="ddad6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddad6-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="ddad6-107">Um ponteiro para a memória externa.</span><span class="sxs-lookup"><span data-stu-id="ddad6-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="ddad6-108">O número de bytes na memória externa.</span><span class="sxs-lookup"><span data-stu-id="ddad6-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="ddad6-109">Um retorno de chamada para quando o objeto for finalizado.</span><span class="sxs-lookup"><span data-stu-id="ddad6-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="ddad6-110">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="ddad6-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="ddad6-111">Estado fornecido pelo usuário que será devolvido para finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="ddad6-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="ddad6-112">O novo `ArrayBuffer` objeto.</span><span class="sxs-lookup"><span data-stu-id="ddad6-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="ddad6-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ddad6-113">Return Value</span></span>  
 <span data-ttu-id="ddad6-114">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="ddad6-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ddad6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddad6-115">Remarks</span></span>  
 <span data-ttu-id="ddad6-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="ddad6-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ddad6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddad6-117">Requirements</span></span>  
 <span data-ttu-id="ddad6-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ddad6-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ddad6-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ddad6-119">See Also</span></span>  
 [<span data-ttu-id="ddad6-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ddad6-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
