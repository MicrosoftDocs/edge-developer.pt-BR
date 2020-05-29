---
description: Cria um `ArrayBuffer` objeto JavaScript para acessar a memória externa.
title: Função JsCreateExternalArrayBuffer | Documentos da Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10561099"
---
# <span data-ttu-id="87a72-103">Função JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="87a72-103">JsCreateExternalArrayBuffer Function</span></span>
<span data-ttu-id="87a72-104">Cria um `ArrayBuffer` objeto JavaScript para acessar a memória externa.</span><span class="sxs-lookup"><span data-stu-id="87a72-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="87a72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87a72-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="87a72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87a72-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="87a72-107">Um ponteiro para a memória externa.</span><span class="sxs-lookup"><span data-stu-id="87a72-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="87a72-108">O número de bytes na memória externa.</span><span class="sxs-lookup"><span data-stu-id="87a72-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="87a72-109">Um retorno de chamada para quando o objeto for finalizado.</span><span class="sxs-lookup"><span data-stu-id="87a72-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="87a72-110">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="87a72-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="87a72-111">Estado fornecido pelo usuário que será devolvido para finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="87a72-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="87a72-112">O novo `ArrayBuffer` objeto.</span><span class="sxs-lookup"><span data-stu-id="87a72-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="87a72-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="87a72-113">Return Value</span></span>  
 <span data-ttu-id="87a72-114">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="87a72-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="87a72-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="87a72-115">Remarks</span></span>  
 <span data-ttu-id="87a72-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="87a72-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="87a72-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87a72-117">Requirements</span></span>  
 <span data-ttu-id="87a72-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="87a72-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="87a72-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="87a72-119">See Also</span></span>  
 [<span data-ttu-id="87a72-120">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="87a72-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)