---
description: Serializa um script analisado para um buffer do que pode ser reutilizado.
title: Função JsSerializeScript | Documentos da Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231932"
---
# <span data-ttu-id="bfd41-103">Função JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="bfd41-103">JsSerializeScript Function</span></span>

<span data-ttu-id="bfd41-104">Serializa um script analisado para um buffer do que pode ser reutilizado.</span><span class="sxs-lookup"><span data-stu-id="bfd41-104">Serializes a parsed script to a buffer than can be reused.</span></span>  
  
## <span data-ttu-id="bfd41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfd41-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### <span data-ttu-id="bfd41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfd41-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="bfd41-107">O script a ser serializado.</span><span class="sxs-lookup"><span data-stu-id="bfd41-107">The script to serialize.</span></span>  
  
 `buffer`  
 <span data-ttu-id="bfd41-108">O buffer no qual colocar o script serializado.</span><span class="sxs-lookup"><span data-stu-id="bfd41-108">The buffer to put the serialized script into.</span></span> <span data-ttu-id="bfd41-109">Pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="bfd41-109">Can be null.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="bfd41-110">Na entrada, o tamanho do buffer, em bytes; em Exit, o tamanho do buffer, em bytes, é necessário para armazenar o script serializado.</span><span class="sxs-lookup"><span data-stu-id="bfd41-110">On entry, the size of the buffer, in bytes; on exit, the size of the buffer, in bytes, required to hold the serialized script.</span></span>  
  
## <span data-ttu-id="bfd41-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bfd41-111">Return Value</span></span>  
 <span data-ttu-id="bfd41-112">O código `JsNoError` se a operação tiver sido bem-sucedida, um código de falha também.</span><span class="sxs-lookup"><span data-stu-id="bfd41-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bfd41-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfd41-113">Remarks</span></span>  
 `JsSerializeScript` <span data-ttu-id="bfd41-114">analisa um script e armazena a forma analisada do script em um formato independente do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bfd41-114">parses a script and then stores the parsed form of the script in a runtime-independent format.</span></span> <span data-ttu-id="bfd41-115">O script serializado pode ser desserializado em qualquer tempo de execução sem exigir que o script seja reanalisado.</span><span class="sxs-lookup"><span data-stu-id="bfd41-115">The serialized script then can be deserialized in any runtime without requiring the script to be re-parsed.</span></span>  
  
 <span data-ttu-id="bfd41-116">Requer um contexto de script ativo.</span><span class="sxs-lookup"><span data-stu-id="bfd41-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bfd41-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfd41-117">Requirements</span></span>  
 <span data-ttu-id="bfd41-118">**Header:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bfd41-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bfd41-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bfd41-119">See Also</span></span>  
 [<span data-ttu-id="bfd41-120">Referência (Runtime do JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bfd41-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
