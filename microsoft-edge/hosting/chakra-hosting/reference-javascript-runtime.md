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
# Referência (tempo de execução JavaScript)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

As APIs do tempo de execução do JavaScript (JsRT) permitem adicionar recursos de script a aplicativos da área de trabalho e do servidor em execução no Windows.  

Se você pretende inserir [ChakraCore](https://github.com/Microsoft/ChakraCore) em seu aplicativo, consulte [ChakraCore wiki](https://aka.ms/corejsrtref) para obter referências de JSRT em vez disso.  

## Nesta seção  

TYPEDEFs, constantes e enumerações que dão suporte à hospedagem JsRT são descritos aqui:  
  
*   [Typedefs, Constantes e Enumerações do Runtime do JavaScript](./javascript-runtime-typedefs-constants-and-enumerations.md)  

As seguintes funções permitem a hospedagem JsRT:  

*   [Função JsAddRef](./jsaddref-function.md)  
*   [Função JsBooleanToBool](./jsbooleantobool-function.md)  
*   [Função JsBoolToBoolean](./jsbooltoboolean-function.md)  
*   [Função JsCallFunction](./jscallfunction-function.md)  
*   [Função JsCollectGarbage](./jscollectgarbage-function.md)  
*   [Função JsConstructObject](./jsconstructobject-function.md)  
*   [Função JsConvertValueToBoolean](./jsconvertvaluetoboolean-function.md)  
*   [Função JsConvertValueToNumber](./jsconvertvaluetonumber-function.md)  
*   [Função JsConvertValueToObject](./jsconvertvaluetoobject-function.md)  
*   [Função JsConvertValueToString](./jsconvertvaluetostring-function.md)  
*   [Função JsCreateArray](./jscreatearray-function.md)  
*   [Função JsCreateArrayBuffer](./jscreatearraybuffer-function.md)  
*   [Função JsCreateContext](./jscreatecontext-function.md)  
*   [Função JsCreateDataView](./jscreatedataview-function.md)  
*   [Função JsCreateError](./jscreateerror-function.md)  
*   [Função JsCreateExternalArrayBuffer](./jscreateexternalarraybuffer-function.md)  
*   [Função JsCreateExternalObject](./jscreateexternalobject-function.md)  
*   [Função JsCreateFunction](./jscreatefunction-function.md)  
*   [Função JsCreateNamedFunction](./jscreatenamedfunction-function.md)  
*   [Função JsCreateObject](./jscreateobject-function.md)  
*   [Função JsCreateRangeError](./jscreaterangeerror-function.md)  
*   [Função JsCreateReferenceError](./jscreatereferenceerror-function.md)  
*   [Função JsCreateRuntime](./jscreateruntime-function.md)  
*   [Função JsCreateSymbol](./jscreatesymbol-function.md)  
*   [Função JsCreateSyntaxError](./jscreatesyntaxerror-function.md)  
*   [Função JsCreateTypeError](./jscreatetypeerror-function.md)  
*   [Função JsCreateTypedArray](./jscreatetypedarray-function.md)  
*   [Função JsCreateURIError](./jscreateurierror-function.md)  
*   [Função JsDefineProperty](./jsdefineproperty-function.md)  
*   [Função JsDeleteIndexedProperty](./jsdeleteindexedproperty-function.md)  
*   [Função JsDeleteProperty](./jsdeleteproperty-function.md)  
*   [Função JsDisableRuntimeExecution](./jsdisableruntimeexecution-function.md)  
*   [Função JsDisposeRuntime](./jsdisposeruntime-function.md)  
*   [Função JsDoubleToNumber](./jsdoubletonumber-function.md)  
*   [Função JsEnableRuntimeExecution](./jsenableruntimeexecution-function.md)  
*   [Função JsEnumerateHeap](./jsenumerateheap-function.md)  
*   [Função JsEquals](./jsequals-function.md)  
*   [Função JsGetAndClearException](./jsgetandclearexception-function.md)  
*   [Função JsGetArrayBufferStorage](./jsgetarraybufferstorage-function.md)  
*   [Função JsGetContextData](./jsgetcontextdata-function.md)  
*   [Função JsGetContextOfObject](./jsgetcontextofobject-function.md)  
*   [Função JsGetCurrentContext](./jsgetcurrentcontext-function.md)  
*   [Função JsGetDataViewStorage](./jsgetdataviewstorage-function.md)  
*   [Função JsGetExtensionAllowed](./jsgetextensionallowed-function.md)  
*   [Função JsGetExternalData](./jsgetexternaldata-function.md)  
*   [Função JsGetFalseValue](./jsgetfalsevalue-function.md)  
*   [Função JsGetGlobalObject](./jsgetglobalobject-function.md)  
*   [Função JsGetIndexedPropertiesExternalData](./jsgetindexedpropertiesexternaldata-function.md)  
*   [Função JsGetIndexedProperty](./jsgetindexedproperty-function.md)  
*   [Função JsGetNullValue](./jsgetnullvalue-function.md)  
*   [Função JsGetOwnPropertyDescriptor](./jsgetownpropertydescriptor-function.md)  
*   [Função JsGetOwnPropertyNames](./jsgetownpropertynames-function.md)  
*   [Função JsGetOwnPropertySymbols](./jsgetownpropertysymbols-function.md)  
*   [Função JsGetProperty](./jsgetproperty-function.md)  
*   [Função JsGetPropertyIdFromName](./jsgetpropertyidfromname-function.md)  
*   [Função JsGetPropertyIdFromSymbol](./jsgetpropertyidfromsymbol-function.md)  
*   [Função JsGetPropertyIdType](./jsgetpropertyidtype-function.md)  
*   [Função JsGetPropertyNameFromId](./jsgetpropertynamefromid-function.md)  
*   [Função JsGetPrototype](./jsgetprototype-function.md)  
*   [Função JsGetRuntime](./jsgetruntime-function.md)  
*   [Função JsGetRuntimeMemoryLimit](./jsgetruntimememorylimit-function.md)  
*   [Função JsGetRuntimeMemoryUsage](./jsgetruntimememoryusage-function.md)  
*   [Função JsGetStringLength](./jsgetstringlength-function.md)  
*   [Função JsGetSymbolFromPropertyId](./jsgetsymbolfrompropertyid-function.md)  
*   [Função JsGetTrueValue](./jsgettruevalue-function.md)  
*   [Função JsGetTypedArrayInfo](./jsgettypedarrayinfo-function.md)  
*   [Função JsGetTypedArrayStorage](./jsgettypedarraystorage-function.md)  
*   [Função JsGetUndefinedValue](./jsgetundefinedvalue-function.md)  
*   [Função JsGetValueType](./jsgetvaluetype-function.md)  
*   [Função JsHasException](./jshasexception-function.md)  
*   [Função JsHasExternalData](./jshasexternaldata-function.md)  
*   [Função JsHasIndexedPropertiesExternalData](./jshasindexedpropertiesexternaldata-function.md)  
*   [Função JsHasIndexedProperty](./jshasindexedproperty-function.md)  
*   [Função JsHasProperty](./jshasproperty-function.md)  
*   [Função JsIdle](./jsidle-function.md)  
*   [Função JsInspectableToObject](./jsinspectabletoobject-function.md)  
*   [Função JsInstanceOf](./jsinstanceof-function.md)  
*   [Função JsIntToNumber](./jsinttonumber-function.md)  
*   [Função JsIsEnumeratingHeap](./jsisenumeratingheap-function.md)  
*   [Função JsIsRuntimeExecutionDisabled](./jsisruntimeexecutiondisabled-function.md)  
*   [Função JsNumberToDouble](./jsnumbertodouble-function.md)  
*   [Função JsNumberToInt](./jsnumbertoint-function.md)  
*   [Função JsObjectToInspectable](./jsobjecttoinspectable-function.md)  
*   [Função JsParseScript](./jsparsescript-function.md)  
*   [Função JsParseSerializedScript](./jsparseserializedscript-function.md)  
*   [Função JsParseSerializedScriptWithCallback](./jsparseserializedscriptwithcallback-function.md)  
*   [Função JsPointerToString](./jspointertostring-function.md)  
*   [Função JsPreventExtension](./jspreventextension-function.md)  
*   [Função JsProjectWinRTNamespace](./jsprojectwinrtnamespace-function.md)  
*   [Função JsRelease](./jsrelease-function.md)  
*   [Função JsRunScript](./jsrunscript-function.md)  
*   [Função JsRunSerializedScript](./jsrunserializedscript-function.md)  
*   [Função JsRunSerializedScriptWithCallback](./jsrunserializedscriptwithcallback-function.md)  
*   [Função JsSerializeScript](./jsserializescript-function.md)  
*   [Função JsSetContextData](./jssetcontextdata-function.md)  
*   [Função JsSetCurrentContext](./jssetcurrentcontext-function.md)  
*   [Função JsSetException](./jssetexception-function.md)  
*   [Função JsSetExternalData](./jssetexternaldata-function.md)  
*   [Função JsSetIndexedPropertiesToExternalData](./jssetindexedpropertiestoexternaldata-function.md)  
*   [Função JsSetIndexedProperty](./jssetindexedproperty-function.md)  
*   [Função JsSetObjectBeforeCollectCallback](./jssetobjectbeforecollectcallback-function.md)  
*   [Função JsSetProjectionEnqueueCallback](./jssetprojectionenqueuecallback-function.md)  
*   [Função JsSetPromiseContinuationCallback](./jssetpromisecontinuationcallback-function.md)  
*   [Função JsSetProperty](./jssetproperty-function.md)  
*   [Função JsSetPrototype](./jssetprototype-function.md)  
*   [Função JsSetRuntimeBeforeCollectCallback](./jssetruntimebeforecollectcallback-function.md)  
*   [Função JsSetRuntimeMemoryAllocationCallback](./jssetruntimememoryallocationcallback-function.md)  
*   [Função JsSetRuntimeMemoryLimit](./jssetruntimememorylimit-function.md)  
*   [Função JsStartDebugging](./jsstartdebugging-function.md)  
*   [Função JsStartProfiling](./jsstartprofiling-function.md)  
*   [Função JsStopProfiling](./jsstopprofiling-function.md)  
*   [Função JsStrictEquals](./jsstrictequals-function.md)  
*   [Função JsStringToPointer](./jsstringtopointer-function.md)  
*   [Função JsValueToVariant](./jsvaluetovariant-function.md)  
*   [Função JsVariantToValue](./jsvarianttovalue-function.md)  

## Consulte também  

*   [Hospedando o Runtime do JavaScript](./hosting-the-javascript-runtime.md)  
*   [Hospedagem de Runtime no JavaScript](../javascript-runtime-hosting.md)  
