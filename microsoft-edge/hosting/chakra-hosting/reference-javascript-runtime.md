---
description: As APIs do tempo de execução do JavaScript (JsRT) permitem adicionar recursos de script a aplicativos da área de trabalho e do servidor em execução no Windows.
title: Referência (Runtime do JavaScript)
ms.date: 06/08/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 7166e6cd5d64060c2939d8404e1415dc34fce17b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752210"
---
# <span data-ttu-id="8333f-103">Referência (tempo de execução JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8333f-103">Reference (JavaScript runtime)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="8333f-104">As APIs do tempo de execução do JavaScript (JsRT) permitem adicionar recursos de script a aplicativos da área de trabalho e do servidor em execução no Windows.</span><span class="sxs-lookup"><span data-stu-id="8333f-104">JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.</span></span>  

<span data-ttu-id="8333f-105">Se você pretende inserir [ChakraCore](https://github.com/Microsoft/ChakraCore) em seu aplicativo, consulte [ChakraCore wiki](https://aka.ms/corejsrtref) para obter referências de JSRT em vez disso.</span><span class="sxs-lookup"><span data-stu-id="8333f-105">If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.</span></span>  

## <span data-ttu-id="8333f-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8333f-106">In this section</span></span>  

<span data-ttu-id="8333f-107">TYPEDEFs, constantes e enumerações que dão suporte à hospedagem JsRT são descritos aqui:</span><span class="sxs-lookup"><span data-stu-id="8333f-107">Typedefs, constants, and enumerations that support JsRT hosting are described here:</span></span>  
  
*   [<span data-ttu-id="8333f-108">Typedefs, Constantes e Enumerações do Runtime do JavaScript</span><span class="sxs-lookup"><span data-stu-id="8333f-108">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>](./javascript-runtime-typedefs-constants-and-enumerations.md)  

<span data-ttu-id="8333f-109">As seguintes funções permitem a hospedagem JsRT:</span><span class="sxs-lookup"><span data-stu-id="8333f-109">The following functions enable JsRT hosting:</span></span>  

*   [<span data-ttu-id="8333f-110">Função JsAddRef</span><span class="sxs-lookup"><span data-stu-id="8333f-110">JsAddRef Function</span></span>](./jsaddref-function.md)  
*   [<span data-ttu-id="8333f-111">Função JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="8333f-111">JsBooleanToBool Function</span></span>](./jsbooleantobool-function.md)  
*   [<span data-ttu-id="8333f-112">Função JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="8333f-112">JsBoolToBoolean Function</span></span>](./jsbooltoboolean-function.md)  
*   [<span data-ttu-id="8333f-113">Função JsCallFunction</span><span class="sxs-lookup"><span data-stu-id="8333f-113">JsCallFunction Function</span></span>](./jscallfunction-function.md)  
*   [<span data-ttu-id="8333f-114">Função JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="8333f-114">JsCollectGarbage Function</span></span>](./jscollectgarbage-function.md)  
*   [<span data-ttu-id="8333f-115">Função JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="8333f-115">JsConstructObject Function</span></span>](./jsconstructobject-function.md)  
*   [<span data-ttu-id="8333f-116">Função JsConvertValueToBoolean</span><span class="sxs-lookup"><span data-stu-id="8333f-116">JsConvertValueToBoolean Function</span></span>](./jsconvertvaluetoboolean-function.md)  
*   [<span data-ttu-id="8333f-117">Função JsConvertValueToNumber</span><span class="sxs-lookup"><span data-stu-id="8333f-117">JsConvertValueToNumber Function</span></span>](./jsconvertvaluetonumber-function.md)  
*   [<span data-ttu-id="8333f-118">Função JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="8333f-118">JsConvertValueToObject Function</span></span>](./jsconvertvaluetoobject-function.md)  
*   [<span data-ttu-id="8333f-119">Função JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="8333f-119">JsConvertValueToString Function</span></span>](./jsconvertvaluetostring-function.md)  
*   [<span data-ttu-id="8333f-120">Função JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="8333f-120">JsCreateArray Function</span></span>](./jscreatearray-function.md)  
*   [<span data-ttu-id="8333f-121">Função JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="8333f-121">JsCreateArrayBuffer Function</span></span>](./jscreatearraybuffer-function.md)  
*   [<span data-ttu-id="8333f-122">Função JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="8333f-122">JsCreateContext Function</span></span>](./jscreatecontext-function.md)  
*   [<span data-ttu-id="8333f-123">Função JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="8333f-123">JsCreateDataView Function</span></span>](./jscreatedataview-function.md)  
*   [<span data-ttu-id="8333f-124">Função JsCreateError</span><span class="sxs-lookup"><span data-stu-id="8333f-124">JsCreateError Function</span></span>](./jscreateerror-function.md)  
*   [<span data-ttu-id="8333f-125">Função JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="8333f-125">JsCreateExternalArrayBuffer Function</span></span>](./jscreateexternalarraybuffer-function.md)  
*   [<span data-ttu-id="8333f-126">Função JsCreateExternalObject</span><span class="sxs-lookup"><span data-stu-id="8333f-126">JsCreateExternalObject Function</span></span>](./jscreateexternalobject-function.md)  
*   [<span data-ttu-id="8333f-127">Função JsCreateFunction</span><span class="sxs-lookup"><span data-stu-id="8333f-127">JsCreateFunction Function</span></span>](./jscreatefunction-function.md)  
*   [<span data-ttu-id="8333f-128">Função JsCreateNamedFunction</span><span class="sxs-lookup"><span data-stu-id="8333f-128">JsCreateNamedFunction Function</span></span>](./jscreatenamedfunction-function.md)  
*   [<span data-ttu-id="8333f-129">Função JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="8333f-129">JsCreateObject Function</span></span>](./jscreateobject-function.md)  
*   [<span data-ttu-id="8333f-130">Função JsCreateRangeError</span><span class="sxs-lookup"><span data-stu-id="8333f-130">JsCreateRangeError Function</span></span>](./jscreaterangeerror-function.md)  
*   [<span data-ttu-id="8333f-131">Função JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="8333f-131">JsCreateReferenceError Function</span></span>](./jscreatereferenceerror-function.md)  
*   [<span data-ttu-id="8333f-132">Função JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="8333f-132">JsCreateRuntime Function</span></span>](./jscreateruntime-function.md)  
*   [<span data-ttu-id="8333f-133">Função JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="8333f-133">JsCreateSymbol Function</span></span>](./jscreatesymbol-function.md)  
*   [<span data-ttu-id="8333f-134">Função JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="8333f-134">JsCreateSyntaxError Function</span></span>](./jscreatesyntaxerror-function.md)  
*   [<span data-ttu-id="8333f-135">Função JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="8333f-135">JsCreateTypeError Function</span></span>](./jscreatetypeerror-function.md)  
*   [<span data-ttu-id="8333f-136">Função JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="8333f-136">JsCreateTypedArray Function</span></span>](./jscreatetypedarray-function.md)  
*   [<span data-ttu-id="8333f-137">Função JsCreateURIError</span><span class="sxs-lookup"><span data-stu-id="8333f-137">JsCreateURIError Function</span></span>](./jscreateurierror-function.md)  
*   [<span data-ttu-id="8333f-138">Função JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-138">JsDefineProperty Function</span></span>](./jsdefineproperty-function.md)  
*   [<span data-ttu-id="8333f-139">Função JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-139">JsDeleteIndexedProperty Function</span></span>](./jsdeleteindexedproperty-function.md)  
*   [<span data-ttu-id="8333f-140">Função JsDeleteProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-140">JsDeleteProperty Function</span></span>](./jsdeleteproperty-function.md)  
*   [<span data-ttu-id="8333f-141">Função JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="8333f-141">JsDisableRuntimeExecution Function</span></span>](./jsdisableruntimeexecution-function.md)  
*   [<span data-ttu-id="8333f-142">Função JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="8333f-142">JsDisposeRuntime Function</span></span>](./jsdisposeruntime-function.md)  
*   [<span data-ttu-id="8333f-143">Função JsDoubleToNumber</span><span class="sxs-lookup"><span data-stu-id="8333f-143">JsDoubleToNumber Function</span></span>](./jsdoubletonumber-function.md)  
*   [<span data-ttu-id="8333f-144">Função JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="8333f-144">JsEnableRuntimeExecution Function</span></span>](./jsenableruntimeexecution-function.md)  
*   [<span data-ttu-id="8333f-145">Função JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="8333f-145">JsEnumerateHeap Function</span></span>](./jsenumerateheap-function.md)  
*   [<span data-ttu-id="8333f-146">Função JsEquals</span><span class="sxs-lookup"><span data-stu-id="8333f-146">JsEquals Function</span></span>](./jsequals-function.md)  
*   [<span data-ttu-id="8333f-147">Função JsGetAndClearException</span><span class="sxs-lookup"><span data-stu-id="8333f-147">JsGetAndClearException Function</span></span>](./jsgetandclearexception-function.md)  
*   [<span data-ttu-id="8333f-148">Função JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="8333f-148">JsGetArrayBufferStorage Function</span></span>](./jsgetarraybufferstorage-function.md)  
*   [<span data-ttu-id="8333f-149">Função JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="8333f-149">JsGetContextData Function</span></span>](./jsgetcontextdata-function.md)  
*   [<span data-ttu-id="8333f-150">Função JsGetContextOfObject</span><span class="sxs-lookup"><span data-stu-id="8333f-150">JsGetContextOfObject Function</span></span>](./jsgetcontextofobject-function.md)  
*   [<span data-ttu-id="8333f-151">Função JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="8333f-151">JsGetCurrentContext Function</span></span>](./jsgetcurrentcontext-function.md)  
*   [<span data-ttu-id="8333f-152">Função JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="8333f-152">JsGetDataViewStorage Function</span></span>](./jsgetdataviewstorage-function.md)  
*   [<span data-ttu-id="8333f-153">Função JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="8333f-153">JsGetExtensionAllowed Function</span></span>](./jsgetextensionallowed-function.md)  
*   [<span data-ttu-id="8333f-154">Função JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="8333f-154">JsGetExternalData Function</span></span>](./jsgetexternaldata-function.md)  
*   [<span data-ttu-id="8333f-155">Função JsGetFalseValue</span><span class="sxs-lookup"><span data-stu-id="8333f-155">JsGetFalseValue Function</span></span>](./jsgetfalsevalue-function.md)  
*   [<span data-ttu-id="8333f-156">Função JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="8333f-156">JsGetGlobalObject Function</span></span>](./jsgetglobalobject-function.md)  
*   [<span data-ttu-id="8333f-157">Função JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="8333f-157">JsGetIndexedPropertiesExternalData Function</span></span>](./jsgetindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="8333f-158">Função JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-158">JsGetIndexedProperty Function</span></span>](./jsgetindexedproperty-function.md)  
*   [<span data-ttu-id="8333f-159">Função JsGetNullValue</span><span class="sxs-lookup"><span data-stu-id="8333f-159">JsGetNullValue Function</span></span>](./jsgetnullvalue-function.md)  
*   [<span data-ttu-id="8333f-160">Função JsGetOwnPropertyDescriptor</span><span class="sxs-lookup"><span data-stu-id="8333f-160">JsGetOwnPropertyDescriptor Function</span></span>](./jsgetownpropertydescriptor-function.md)  
*   [<span data-ttu-id="8333f-161">Função JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="8333f-161">JsGetOwnPropertyNames Function</span></span>](./jsgetownpropertynames-function.md)  
*   [<span data-ttu-id="8333f-162">Função JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="8333f-162">JsGetOwnPropertySymbols Function</span></span>](./jsgetownpropertysymbols-function.md)  
*   [<span data-ttu-id="8333f-163">Função JsGetProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-163">JsGetProperty Function</span></span>](./jsgetproperty-function.md)  
*   [<span data-ttu-id="8333f-164">Função JsGetPropertyIdFromName</span><span class="sxs-lookup"><span data-stu-id="8333f-164">JsGetPropertyIdFromName Function</span></span>](./jsgetpropertyidfromname-function.md)  
*   [<span data-ttu-id="8333f-165">Função JsGetPropertyIdFromSymbol</span><span class="sxs-lookup"><span data-stu-id="8333f-165">JsGetPropertyIdFromSymbol Function</span></span>](./jsgetpropertyidfromsymbol-function.md)  
*   [<span data-ttu-id="8333f-166">Função JsGetPropertyIdType</span><span class="sxs-lookup"><span data-stu-id="8333f-166">JsGetPropertyIdType Function</span></span>](./jsgetpropertyidtype-function.md)  
*   [<span data-ttu-id="8333f-167">Função JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="8333f-167">JsGetPropertyNameFromId Function</span></span>](./jsgetpropertynamefromid-function.md)  
*   [<span data-ttu-id="8333f-168">Função JsGetPrototype</span><span class="sxs-lookup"><span data-stu-id="8333f-168">JsGetPrototype Function</span></span>](./jsgetprototype-function.md)  
*   [<span data-ttu-id="8333f-169">Função JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="8333f-169">JsGetRuntime Function</span></span>](./jsgetruntime-function.md)  
*   [<span data-ttu-id="8333f-170">Função JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="8333f-170">JsGetRuntimeMemoryLimit Function</span></span>](./jsgetruntimememorylimit-function.md)  
*   [<span data-ttu-id="8333f-171">Função JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="8333f-171">JsGetRuntimeMemoryUsage Function</span></span>](./jsgetruntimememoryusage-function.md)  
*   [<span data-ttu-id="8333f-172">Função JsGetStringLength</span><span class="sxs-lookup"><span data-stu-id="8333f-172">JsGetStringLength Function</span></span>](./jsgetstringlength-function.md)  
*   [<span data-ttu-id="8333f-173">Função JsGetSymbolFromPropertyId</span><span class="sxs-lookup"><span data-stu-id="8333f-173">JsGetSymbolFromPropertyId Function</span></span>](./jsgetsymbolfrompropertyid-function.md)  
*   [<span data-ttu-id="8333f-174">Função JsGetTrueValue</span><span class="sxs-lookup"><span data-stu-id="8333f-174">JsGetTrueValue Function</span></span>](./jsgettruevalue-function.md)  
*   [<span data-ttu-id="8333f-175">Função JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="8333f-175">JsGetTypedArrayInfo Function</span></span>](./jsgettypedarrayinfo-function.md)  
*   [<span data-ttu-id="8333f-176">Função JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="8333f-176">JsGetTypedArrayStorage Function</span></span>](./jsgettypedarraystorage-function.md)  
*   [<span data-ttu-id="8333f-177">Função JsGetUndefinedValue</span><span class="sxs-lookup"><span data-stu-id="8333f-177">JsGetUndefinedValue Function</span></span>](./jsgetundefinedvalue-function.md)  
*   [<span data-ttu-id="8333f-178">Função JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="8333f-178">JsGetValueType Function</span></span>](./jsgetvaluetype-function.md)  
*   [<span data-ttu-id="8333f-179">Função JsHasException</span><span class="sxs-lookup"><span data-stu-id="8333f-179">JsHasException Function</span></span>](./jshasexception-function.md)  
*   [<span data-ttu-id="8333f-180">Função JsHasExternalData</span><span class="sxs-lookup"><span data-stu-id="8333f-180">JsHasExternalData Function</span></span>](./jshasexternaldata-function.md)  
*   [<span data-ttu-id="8333f-181">Função JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="8333f-181">JsHasIndexedPropertiesExternalData Function</span></span>](./jshasindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="8333f-182">Função JsHasIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-182">JsHasIndexedProperty Function</span></span>](./jshasindexedproperty-function.md)  
*   [<span data-ttu-id="8333f-183">Função JsHasProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-183">JsHasProperty Function</span></span>](./jshasproperty-function.md)  
*   [<span data-ttu-id="8333f-184">Função JsIdle</span><span class="sxs-lookup"><span data-stu-id="8333f-184">JsIdle Function</span></span>](./jsidle-function.md)  
*   [<span data-ttu-id="8333f-185">Função JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="8333f-185">JsInspectableToObject Function</span></span>](./jsinspectabletoobject-function.md)  
*   [<span data-ttu-id="8333f-186">Função JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="8333f-186">JsInstanceOf Function</span></span>](./jsinstanceof-function.md)  
*   [<span data-ttu-id="8333f-187">Função JsIntToNumber</span><span class="sxs-lookup"><span data-stu-id="8333f-187">JsIntToNumber Function</span></span>](./jsinttonumber-function.md)  
*   [<span data-ttu-id="8333f-188">Função JsIsEnumeratingHeap</span><span class="sxs-lookup"><span data-stu-id="8333f-188">JsIsEnumeratingHeap Function</span></span>](./jsisenumeratingheap-function.md)  
*   [<span data-ttu-id="8333f-189">Função JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="8333f-189">JsIsRuntimeExecutionDisabled Function</span></span>](./jsisruntimeexecutiondisabled-function.md)  
*   [<span data-ttu-id="8333f-190">Função JsNumberToDouble</span><span class="sxs-lookup"><span data-stu-id="8333f-190">JsNumberToDouble Function</span></span>](./jsnumbertodouble-function.md)  
*   [<span data-ttu-id="8333f-191">Função JsNumberToInt</span><span class="sxs-lookup"><span data-stu-id="8333f-191">JsNumberToInt Function</span></span>](./jsnumbertoint-function.md)  
*   [<span data-ttu-id="8333f-192">Função JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="8333f-192">JsObjectToInspectable Function</span></span>](./jsobjecttoinspectable-function.md)  
*   [<span data-ttu-id="8333f-193">Função JsParseScript</span><span class="sxs-lookup"><span data-stu-id="8333f-193">JsParseScript Function</span></span>](./jsparsescript-function.md)  
*   [<span data-ttu-id="8333f-194">Função JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="8333f-194">JsParseSerializedScript Function</span></span>](./jsparseserializedscript-function.md)  
*   [<span data-ttu-id="8333f-195">Função JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="8333f-195">JsParseSerializedScriptWithCallback Function</span></span>](./jsparseserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="8333f-196">Função JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="8333f-196">JsPointerToString Function</span></span>](./jspointertostring-function.md)  
*   [<span data-ttu-id="8333f-197">Função JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="8333f-197">JsPreventExtension Function</span></span>](./jspreventextension-function.md)  
*   [<span data-ttu-id="8333f-198">Função JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="8333f-198">JsProjectWinRTNamespace Function</span></span>](./jsprojectwinrtnamespace-function.md)  
*   [<span data-ttu-id="8333f-199">Função JsRelease</span><span class="sxs-lookup"><span data-stu-id="8333f-199">JsRelease Function</span></span>](./jsrelease-function.md)  
*   [<span data-ttu-id="8333f-200">Função JsRunScript</span><span class="sxs-lookup"><span data-stu-id="8333f-200">JsRunScript Function</span></span>](./jsrunscript-function.md)  
*   [<span data-ttu-id="8333f-201">Função JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="8333f-201">JsRunSerializedScript Function</span></span>](./jsrunserializedscript-function.md)  
*   [<span data-ttu-id="8333f-202">Função JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="8333f-202">JsRunSerializedScriptWithCallback Function</span></span>](./jsrunserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="8333f-203">Função JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="8333f-203">JsSerializeScript Function</span></span>](./jsserializescript-function.md)  
*   [<span data-ttu-id="8333f-204">Função JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="8333f-204">JsSetContextData Function</span></span>](./jssetcontextdata-function.md)  
*   [<span data-ttu-id="8333f-205">Função JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="8333f-205">JsSetCurrentContext Function</span></span>](./jssetcurrentcontext-function.md)  
*   [<span data-ttu-id="8333f-206">Função JsSetException</span><span class="sxs-lookup"><span data-stu-id="8333f-206">JsSetException Function</span></span>](./jssetexception-function.md)  
*   [<span data-ttu-id="8333f-207">Função JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="8333f-207">JsSetExternalData Function</span></span>](./jssetexternaldata-function.md)  
*   [<span data-ttu-id="8333f-208">Função JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="8333f-208">JsSetIndexedPropertiesToExternalData Function</span></span>](./jssetindexedpropertiestoexternaldata-function.md)  
*   [<span data-ttu-id="8333f-209">Função JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-209">JsSetIndexedProperty Function</span></span>](./jssetindexedproperty-function.md)  
*   [<span data-ttu-id="8333f-210">Função JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="8333f-210">JsSetObjectBeforeCollectCallback Function</span></span>](./jssetobjectbeforecollectcallback-function.md)  
*   [<span data-ttu-id="8333f-211">Função JsSetProjectionEnqueueCallback</span><span class="sxs-lookup"><span data-stu-id="8333f-211">JsSetProjectionEnqueueCallback Function</span></span>](./jssetprojectionenqueuecallback-function.md)  
*   [<span data-ttu-id="8333f-212">Função JsSetPromiseContinuationCallback</span><span class="sxs-lookup"><span data-stu-id="8333f-212">JsSetPromiseContinuationCallback Function</span></span>](./jssetpromisecontinuationcallback-function.md)  
*   [<span data-ttu-id="8333f-213">Função JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="8333f-213">JsSetProperty Function</span></span>](./jssetproperty-function.md)  
*   [<span data-ttu-id="8333f-214">Função JsSetPrototype</span><span class="sxs-lookup"><span data-stu-id="8333f-214">JsSetPrototype Function</span></span>](./jssetprototype-function.md)  
*   [<span data-ttu-id="8333f-215">Função JsSetRuntimeBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="8333f-215">JsSetRuntimeBeforeCollectCallback Function</span></span>](./jssetruntimebeforecollectcallback-function.md)  
*   [<span data-ttu-id="8333f-216">Função JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="8333f-216">JsSetRuntimeMemoryAllocationCallback Function</span></span>](./jssetruntimememoryallocationcallback-function.md)  
*   [<span data-ttu-id="8333f-217">Função JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="8333f-217">JsSetRuntimeMemoryLimit Function</span></span>](./jssetruntimememorylimit-function.md)  
*   [<span data-ttu-id="8333f-218">Função JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="8333f-218">JsStartDebugging Function</span></span>](./jsstartdebugging-function.md)  
*   [<span data-ttu-id="8333f-219">Função JsStartProfiling</span><span class="sxs-lookup"><span data-stu-id="8333f-219">JsStartProfiling Function</span></span>](./jsstartprofiling-function.md)  
*   [<span data-ttu-id="8333f-220">Função JsStopProfiling</span><span class="sxs-lookup"><span data-stu-id="8333f-220">JsStopProfiling Function</span></span>](./jsstopprofiling-function.md)  
*   [<span data-ttu-id="8333f-221">Função JsStrictEquals</span><span class="sxs-lookup"><span data-stu-id="8333f-221">JsStrictEquals Function</span></span>](./jsstrictequals-function.md)  
*   [<span data-ttu-id="8333f-222">Função JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="8333f-222">JsStringToPointer Function</span></span>](./jsstringtopointer-function.md)  
*   [<span data-ttu-id="8333f-223">Função JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="8333f-223">JsValueToVariant Function</span></span>](./jsvaluetovariant-function.md)  
*   [<span data-ttu-id="8333f-224">Função JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="8333f-224">JsVariantToValue Function</span></span>](./jsvarianttovalue-function.md)  

## <span data-ttu-id="8333f-225">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8333f-225">See also</span></span>  

*   [<span data-ttu-id="8333f-226">Hospedando o Runtime do JavaScript</span><span class="sxs-lookup"><span data-stu-id="8333f-226">Hosting the JavaScript Runtime</span></span>](./hosting-the-javascript-runtime.md)  
*   [<span data-ttu-id="8333f-227">Hospedagem de Runtime no JavaScript</span><span class="sxs-lookup"><span data-stu-id="8333f-227">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)  
