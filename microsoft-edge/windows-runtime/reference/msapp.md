---
title: Referência de API MSApp
description: Fornece funções auxiliares que permitem criar objetos BLOB e MSStream. Os objetos e membros do MSApp têm suporte para aplicativos do Windows que usam JavaScript.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carregamento de arquivo, blog, MSStream, aplicativos do Windows 10, UWP, Edge
ms.openlocfilehash: 0ed8cefa918bd44f3b2c4e8312d2c1d3b4ace8fc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10562519"
---
# <span data-ttu-id="e3a04-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="e3a04-105">MSApp</span></span>

<span data-ttu-id="e3a04-106">O objeto MSApp e seus membros têm suporte somente para aplicativos do Windows que usam JavaScript (incluindo PWAs acessando recursos da API do Windows).</span><span class="sxs-lookup"><span data-stu-id="e3a04-106">The MSApp object and its members are supported only for Windows apps using JavaScript (including PWAs accessing Windows API features).</span></span> <span data-ttu-id="e3a04-107">O objeto MSApp existe somente no contexto local de um documento HTML em um aplicativo do Windows carregado por meio do esquema de URI MS-Appx; caso contrário, o objeto não existe (e conseqüentemente, nenhum de seus métodos e propriedades estão disponíveis).</span><span class="sxs-lookup"><span data-stu-id="e3a04-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>

<span data-ttu-id="e3a04-108">Ele fornece funções auxiliares que permitem criar objetos [blob](https://developer.mozilla.org/docs/Web/API/Blob) e [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="e3a04-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**<span data-ttu-id="e3a04-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3a04-109">Methods</span></span>**](#msapp-methods) | <span data-ttu-id="e3a04-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getviewid](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="e3a04-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span> |

| | |
| :--- | :--- |
| [**<span data-ttu-id="e3a04-111">:</span><span class="sxs-lookup"><span data-stu-id="e3a04-111">Constants</span></span>**](#msapp-constants) | <span data-ttu-id="e3a04-112">[atual](#current), [alto](#high), [ocioso](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="e3a04-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>|

| | |
| :--- | :--- |
| [<span data-ttu-id="e3a04-113">Interface **MSAppAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="e3a04-113">**MSAppAsyncOperation** interface</span></span>](#msappasyncoperation) | [<span data-ttu-id="e3a04-114">start</span><span class="sxs-lookup"><span data-stu-id="e3a04-114">start</span></span>](#start) |

## <span data-ttu-id="e3a04-115">Métodos MSApp</span><span class="sxs-lookup"><span data-stu-id="e3a04-115">MSApp Methods</span></span>

### <span data-ttu-id="e3a04-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="e3a04-116">clearTemporaryWebDataAsync</span></span> 
<span data-ttu-id="e3a04-117">Limpa o cache e os dados do indexedDB para o aplicativo ou [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="e3a04-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### <span data-ttu-id="e3a04-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-118">Parameters</span></span>
<span data-ttu-id="e3a04-119">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e3a04-119">This method has no parameters.</span></span>

#### <span data-ttu-id="e3a04-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-120">Return value</span></span>
<span data-ttu-id="e3a04-121">Digite[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="e3a04-121">Type: [`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span></span>

<span data-ttu-id="e3a04-122">Representa uma ação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e3a04-122">Represents an asynchronous action.</span></span>

### <span data-ttu-id="e3a04-123">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="e3a04-123">createBlobFromRandomAccessStream</span></span>
<span data-ttu-id="e3a04-124">Cria um [blob](https://developer.mozilla.org/docs/Web/API/Blob) a partir de um [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) objeto.</span><span class="sxs-lookup"><span data-stu-id="e3a04-124">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span> <span data-ttu-id="e3a04-125">Esse método deve ser usado ao lidar com `IRandomAccessStream` objetos em aplicativos para criar um objeto baseado no W3C a partir do Stream.</span><span class="sxs-lookup"><span data-stu-id="e3a04-125">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span> <span data-ttu-id="e3a04-126">Depois que o blob é criado, ele pode ser usado com o [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [APIs de URL](https://developer.mozilla.org/docs/Web/API/URL)e [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="e3a04-126">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span> 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### <span data-ttu-id="e3a04-127">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-127">Parameters</span></span>

`type` <span data-ttu-id="e3a04-128">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-128">[in]</span></span>

|<span data-ttu-id="e3a04-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-129">Type</span></span> | <span data-ttu-id="e3a04-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-130">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-131">String</span><span class="sxs-lookup"><span data-stu-id="e3a04-131">String</span></span> | <span data-ttu-id="e3a04-132">Tipo de conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="e3a04-132">Content type of the data.</span></span> <span data-ttu-id="e3a04-133">Essa cadeia de caracteres deve estar no formato especificado no token do tipo de mídia definido na seção 3,7 da RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="e3a04-133">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>

`stream` <span data-ttu-id="e3a04-134">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-134">[in]</span></span>

|<span data-ttu-id="e3a04-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-135">Type</span></span> | <span data-ttu-id="e3a04-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-136">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-137">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-137">Any</span></span> | <span data-ttu-id="e3a04-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) a ser armazenado no BLOB.</span><span class="sxs-lookup"><span data-stu-id="e3a04-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>

#### <span data-ttu-id="e3a04-139">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-139">Return value</span></span>
|<span data-ttu-id="e3a04-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-140">Type</span></span> | <span data-ttu-id="e3a04-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-141">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-142">Irregular</span><span class="sxs-lookup"><span data-stu-id="e3a04-142">Blob</span></span> | <span data-ttu-id="e3a04-143">Novo objeto BLOB que contém o fluxo.</span><span class="sxs-lookup"><span data-stu-id="e3a04-143">New blob object that contains the stream.</span></span>

#### <span data-ttu-id="e3a04-144">Exceções</span><span class="sxs-lookup"><span data-stu-id="e3a04-144">Exceptions</span></span>
|<span data-ttu-id="e3a04-145">Extremamente</span><span class="sxs-lookup"><span data-stu-id="e3a04-145">Exception</span></span> | <span data-ttu-id="e3a04-146">Condição</span><span class="sxs-lookup"><span data-stu-id="e3a04-146">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-147">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="e3a04-147">TypeMismatchError</span></span> | <span data-ttu-id="e3a04-148">O tipo de nó é incompatível com o tipo de parâmetro esperado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-148">The node type is incompatible with the expected parameter type.</span></span> <span data-ttu-id="e3a04-149">Para versões anteriores ao Internet Explorer 10, TYPE_MISMATCH_ERR é retornado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-149">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

#### <span data-ttu-id="e3a04-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-150">Remarks</span></span>
<span data-ttu-id="e3a04-151">Cria um blob a partir de tipos do Windows Runtime por meio do namespace MSApp no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="e3a04-151">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span> <span data-ttu-id="e3a04-152">Esse método criará um blob que é essencialmente um wrapper claro sobre o [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) objeto fornecido a ele.</span><span class="sxs-lookup"><span data-stu-id="e3a04-152">This method will create a blob that is essentially a light wrapper over the [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span> <span data-ttu-id="e3a04-153">O blob é proprietário do tempo de vida desse fluxo e o fluxo será fechado quando o blob for destruído.</span><span class="sxs-lookup"><span data-stu-id="e3a04-153">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span> 

#### <span data-ttu-id="e3a04-154">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-154">Example</span></span>

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### <span data-ttu-id="e3a04-155">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="e3a04-155">createDataPackage</span></span>
<span data-ttu-id="e3a04-156">Converte o intervalo especificado do usuário ou do aplicativo em um fragmento de HTML que pode ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-156">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### <span data-ttu-id="e3a04-157">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-157">Parameters</span></span>
`object` <span data-ttu-id="e3a04-158">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-158">[in]</span></span>

|<span data-ttu-id="e3a04-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-159">Type</span></span> | <span data-ttu-id="e3a04-160">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-160">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-161">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-161">Any</span></span> | <span data-ttu-id="e3a04-162">Esse intervalo pode ser criado a partir de um objeto Selection, por exemplo: `window.selection.getRangeAt(0)` ou manualmente.</span><span class="sxs-lookup"><span data-stu-id="e3a04-162">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>

#### <span data-ttu-id="e3a04-163">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-163">Return value</span></span>
|<span data-ttu-id="e3a04-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-164">Type</span></span> | <span data-ttu-id="e3a04-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-165">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-166">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-166">Any</span></span> | <span data-ttu-id="e3a04-167">Contém a marcação HTML para o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-167">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="e3a04-168">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-168">Remarks</span></span>
<span data-ttu-id="e3a04-169">Esse método oferece suporte somente ao [intervalo dom](https://developer.mozilla.org/docs/Web/API/Range), e não a [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="e3a04-169">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span> <span data-ttu-id="e3a04-170">O pacote de dados retornado para o intervalo especificado contém marcação HTML no formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="e3a04-170">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>

<span data-ttu-id="e3a04-171">Não há propriedades disponíveis para o pacote de dados retornado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-171">There are no available properties for the returned data package.</span></span>

### <span data-ttu-id="e3a04-172">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="e3a04-172">createDataPackageFromSelection</span></span> 
<span data-ttu-id="e3a04-173">Converte a seleção do usuário ou do aplicativo em um fragmento HTML que pode ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-173">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### <span data-ttu-id="e3a04-174">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-174">Parameters</span></span>
<span data-ttu-id="e3a04-175">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e3a04-175">This method has no parameters.</span></span>

#### <span data-ttu-id="e3a04-176">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-176">Return value</span></span>
|<span data-ttu-id="e3a04-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-177">Type</span></span> | <span data-ttu-id="e3a04-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-178">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-179">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-179">Any</span></span> | <span data-ttu-id="e3a04-180">Contém a marcação HTML para o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-180">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="e3a04-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-181">Remarks</span></span>
<span data-ttu-id="e3a04-182">O pacote de dados retornado para a seleção contém marcação HTML no formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="e3a04-182">The returned data package for the selection contains HTML markup in clipboard format.</span></span> <span data-ttu-id="e3a04-183">Se não houver nenhuma seleção de usuário em qualquer lugar dentro da interface do usuário do aplicativo, o `createDataPackageFromSelection` retorna NULL.</span><span class="sxs-lookup"><span data-stu-id="e3a04-183">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns null.</span></span>

<span data-ttu-id="e3a04-184">Não há propriedades disponíveis para o pacote de dados retornado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-184">There are no available properties for the returned data package.</span></span>
 
### <span data-ttu-id="e3a04-185">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="e3a04-185">createFileFromStorageFile</span></span> 
<span data-ttu-id="e3a04-186">Converte um [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) em um objeto W3C padrão [`File`](https://developer.mozilla.org/docs/Web/API/File) .</span><span class="sxs-lookup"><span data-stu-id="e3a04-186">Converts a [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) to a standard W3C [`File`](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### <span data-ttu-id="e3a04-187">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-187">Parameters</span></span>
`storageFile` <span data-ttu-id="e3a04-188">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-188">[in]</span></span>

|<span data-ttu-id="e3a04-189">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-189">Type</span></span> | <span data-ttu-id="e3a04-190">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-190">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-191">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-191">Any</span></span> | <span data-ttu-id="e3a04-192">Contém o arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3a04-192">Contains the storage file.</span></span>

#### <span data-ttu-id="e3a04-193">Exceções</span><span class="sxs-lookup"><span data-stu-id="e3a04-193">Exceptions</span></span>
|<span data-ttu-id="e3a04-194">Extremamente</span><span class="sxs-lookup"><span data-stu-id="e3a04-194">Exception</span></span> | <span data-ttu-id="e3a04-195">Condição</span><span class="sxs-lookup"><span data-stu-id="e3a04-195">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-196">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="e3a04-196">TypeMismatchError</span></span> | <span data-ttu-id="e3a04-197">A referência do arquivo W3C especificado é inválida.</span><span class="sxs-lookup"><span data-stu-id="e3a04-197">The specified W3C file reference is invalid.</span></span> <span data-ttu-id="e3a04-198">Para versões anteriores ao Internet Explorer 10, TYPE_MISMATCH_ERR é retornado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-198">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

### <span data-ttu-id="e3a04-199">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="e3a04-199">createStreamFromInputStream</span></span>  

<span data-ttu-id="e3a04-200">Cria um [`MSStream`](https://msdn.microsoft.com/library/hh772328) de [`InputStream`](https://msdn.microsoft.com/library/hh772327) .</span><span class="sxs-lookup"><span data-stu-id="e3a04-200">Creates an [`MSStream`](https://msdn.microsoft.com/library/hh772328) from an [`InputStream`](https://msdn.microsoft.com/library/hh772327).</span></span>  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### <span data-ttu-id="e3a04-201">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-201">Parameters</span></span>
`type` <span data-ttu-id="e3a04-202">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-202">[in]</span></span>

|<span data-ttu-id="e3a04-203">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-203">Type</span></span> | <span data-ttu-id="e3a04-204">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-204">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-205">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-205">DOMString</span></span> | <span data-ttu-id="e3a04-206">Tipo de conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="e3a04-206">Content type of the data.</span></span> <span data-ttu-id="e3a04-207">Essa cadeia de caracteres deve estar no formato especificado no token do tipo de mídia definido na seção 3,7 da RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="e3a04-207">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span> <span data-ttu-id="e3a04-208">([Veja tipos MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. text/plain, text/html, image/jpeg, image/png, Audio/MPEG, Audio/OGG, Audio/\*, Video/MP4, etc.).</span><span class="sxs-lookup"><span data-stu-id="e3a04-208">([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) ie. text/plain, text/html, image/jpeg, image/png, audio/mpeg, audio/ogg, audio/\*, video/mp4, etc.).</span></span> 

`inputStream` <span data-ttu-id="e3a04-209">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-209">[in]</span></span>

|<span data-ttu-id="e3a04-210">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-210">Type</span></span> | <span data-ttu-id="e3a04-211">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-211">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-212">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-212">Any</span></span> | <span data-ttu-id="e3a04-213">A [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) a ser armazenada no `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-213">The [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>

#### <span data-ttu-id="e3a04-214">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-214">Remarks</span></span>
<span data-ttu-id="e3a04-215">Esse método assume um tipo de conteúdo e a `IInputStream` referência.</span><span class="sxs-lookup"><span data-stu-id="e3a04-215">This method takes a content-type, and the `IInputStream` reference.</span></span> <span data-ttu-id="e3a04-216">Em seguida, o método verifica se a referência do fluxo transmitida é uma instância do tipo `IInputStream` e, se não for, throws `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-216">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span> <span data-ttu-id="e3a04-217">Se não ocorrerem erros, `createStreamFromInputStream` o cria uma `MSStream` (a partir de suas entradas).</span><span class="sxs-lookup"><span data-stu-id="e3a04-217">If no error occurs, `createStreamFromInputStream` creates an `MSStream` (from its inputs).</span></span>

#### <span data-ttu-id="e3a04-218">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-218">Example</span></span>
<span data-ttu-id="e3a04-219">Um `IInputStream` pode ser usado para criar um `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-219">An `IInputStream` can be used to create an `MSStream`.</span></span> <span data-ttu-id="e3a04-220">Como `MSStreams` são objetos inerentemente de uso único, todas as URLs criadas por `URL.createObjectURL` são revogadas na primeira vez que são resolvidas pelo elemento Image.</span><span class="sxs-lookup"><span data-stu-id="e3a04-220">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span> <span data-ttu-id="e3a04-221">Além disso, as solicitações para uma segunda URL neste objeto após o fluxo ter sido usado falharão.</span><span class="sxs-lookup"><span data-stu-id="e3a04-221">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### <span data-ttu-id="e3a04-222">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="e3a04-222">execAsyncAtPriority</span></span> 
<span data-ttu-id="e3a04-223">Agenda um retorno de chamada para ser executado em um momento posterior, de acordo com a prioridade determinada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-223">Schedules a callback to be executed at a later time according to the given priority.</span></span> 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### <span data-ttu-id="e3a04-224">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-224">Parameters</span></span>
`asynchronousCallback` <span data-ttu-id="e3a04-225">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-225">[in]</span></span>

|<span data-ttu-id="e3a04-226">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-226">Type</span></span> | <span data-ttu-id="e3a04-227">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-227">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-228">Função</span><span class="sxs-lookup"><span data-stu-id="e3a04-228">Function</span></span> | <span data-ttu-id="e3a04-229">A função de retorno de chamada para ser executada de forma assíncrona, despachada com a prioridade determinada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-229">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>

`priority` <span data-ttu-id="e3a04-230">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-230">[in]</span></span>

|<span data-ttu-id="e3a04-231">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-231">Type</span></span> | <span data-ttu-id="e3a04-232">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-232">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-233">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-233">DOMString</span></span> | <span data-ttu-id="e3a04-234">O valor de prioridade contextual no qual o retorno de chamada do asynchronousCallback é executado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-234">The contextual priority value at which the asynchronousCallback callback is run.</span></span> <span data-ttu-id="e3a04-235">Consulte [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="e3a04-235">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="e3a04-236">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-236">[in]</span></span>

|<span data-ttu-id="e3a04-237">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-237">Type</span></span> | <span data-ttu-id="e3a04-238">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-238">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-239">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-239">Any</span></span> | <span data-ttu-id="e3a04-240">Uma série opcional de argumentos que são passados para a função de retorno de chamada synchronousCallback (como parâmetros 1 e on).</span><span class="sxs-lookup"><span data-stu-id="e3a04-240">An optional series of arguments that are passed to the synchronousCallback callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="e3a04-241">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-241">Return value</span></span>
<span data-ttu-id="e3a04-242">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e3a04-242">This method does not return a value.</span></span>

#### <span data-ttu-id="e3a04-243">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-243">Remarks</span></span>
<span data-ttu-id="e3a04-244">A `asynchronousCallback` função de retorno de chamada fornecida será executada de forma assíncrona mais tarde.</span><span class="sxs-lookup"><span data-stu-id="e3a04-244">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span> `asynchronousCallback` <span data-ttu-id="e3a04-245">será despachado de acordo com a prioridade fornecida.</span><span class="sxs-lookup"><span data-stu-id="e3a04-245">will be dispatched according to the provided priority.</span></span> <span data-ttu-id="e3a04-246">A prioridade normal equivale ao método existente [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) .</span><span class="sxs-lookup"><span data-stu-id="e3a04-246">Normal priority is equivalent to the existing [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span> <span data-ttu-id="e3a04-247">Quando o retorno de chamada é executado, a prioridade contextual atual é definida como o valor de parâmetro de prioridade fornecido para a duração da execução do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-247">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>

<span data-ttu-id="e3a04-248">O `asynchronousCallback` parâmetro callback pode ser qualquer função.</span><span class="sxs-lookup"><span data-stu-id="e3a04-248">The `asynchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="e3a04-249">Se os argumentos forem fornecidos após o `priority` parâmetro, todos serão passados para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-249">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>

<span data-ttu-id="e3a04-250">Ao contrário `execAtPriority` , qualquer objeto retornado pela `asynchronousCallback` função de retorno de chamada é ignorado (e não é retornado via `execAsyncAtPriority` ).</span><span class="sxs-lookup"><span data-stu-id="e3a04-250">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored (and not returned via `execAsyncAtPriority`).</span></span>

### <span data-ttu-id="e3a04-251">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="e3a04-251">execAtPriority</span></span> 
<span data-ttu-id="e3a04-252">Executa a função de retorno de chamada especificada na prioridade contextual determinada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-252">Runs the specified callback function at the given contextual priority.</span></span>

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### <span data-ttu-id="e3a04-253">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-253">Parameters</span></span>
`synchronousCallback` <span data-ttu-id="e3a04-254">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-254">[in]</span></span>

|<span data-ttu-id="e3a04-255">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-255">Type</span></span> | <span data-ttu-id="e3a04-256">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-256">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-257">Função</span><span class="sxs-lookup"><span data-stu-id="e3a04-257">Function</span></span> | <span data-ttu-id="e3a04-258">A função de retorno de chamada a ser executada de forma síncrona na prioridade contextual determinada prioridade.</span><span class="sxs-lookup"><span data-stu-id="e3a04-258">The callback function to run synchronously at the given priority contextual priority.</span></span>

`priority` <span data-ttu-id="e3a04-259">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-259">[in]</span></span>

|<span data-ttu-id="e3a04-260">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-260">Type</span></span> | <span data-ttu-id="e3a04-261">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-261">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-262">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-262">DOMString</span></span> | <span data-ttu-id="e3a04-263">O valor de prioridade especificado ao qual o valor de prioridade contextual atual será definido ao executar a `synchronousCallback` função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-263">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span> <span data-ttu-id="e3a04-264">Consulte [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="e3a04-264">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="e3a04-265">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-265">[in]</span></span>

|<span data-ttu-id="e3a04-266">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-266">Type</span></span> | <span data-ttu-id="e3a04-267">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-267">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-268">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-268">Any</span></span> | <span data-ttu-id="e3a04-269">Uma série opcional de argumentos que são passados para a `synchronousCallback` função de retorno de chamada (como parâmetros 1 e ativado).</span><span class="sxs-lookup"><span data-stu-id="e3a04-269">An optional series of arguments that are passed to the `synchronousCallback` callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="e3a04-270">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-270">Return value</span></span>
|<span data-ttu-id="e3a04-271">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-271">Type</span></span> | <span data-ttu-id="e3a04-272">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-272">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-273">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-273">Any</span></span> | <span data-ttu-id="e3a04-274">Retorna o valor de retorno do `synchronousCallback` retorno de chamada (conforme aplicável).</span><span class="sxs-lookup"><span data-stu-id="e3a04-274">Returns the return value of the `synchronousCallback` callback (as applicable).</span></span>

#### <span data-ttu-id="e3a04-275">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-275">Remarks</span></span>
<span data-ttu-id="e3a04-276">O `synchronousCallback` método callback fornecido é executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="e3a04-276">The provided `synchronousCallback` callback method is execute synchronously.</span></span> <span data-ttu-id="e3a04-277">A prioridade contextual atual é alterada para o valor de prioridade fornecido (fornecido pelo argumento Priority) para a duração da função de retorno de chamada fornecida.</span><span class="sxs-lookup"><span data-stu-id="e3a04-277">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span> <span data-ttu-id="e3a04-278">Depois que a execução da função de retorno de chamada terminar, a prioridade será retornada ao valor anterior antes da `execAtPriority` chamada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-278">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span> <span data-ttu-id="e3a04-279">O valor de retorno `execAtPriority` é o valor de retorno do método callback (conforme fornecido).</span><span class="sxs-lookup"><span data-stu-id="e3a04-279">The return value from `execAtPriority` is the return value of the callback method (as provided).</span></span>
 
<span data-ttu-id="e3a04-280">O `synchronousCallback` parâmetro callback pode ser qualquer função.</span><span class="sxs-lookup"><span data-stu-id="e3a04-280">The `synchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="e3a04-281">Se algum argumento for fornecido após o parâmetro Priority, ele será passado para o método callback fornecido.</span><span class="sxs-lookup"><span data-stu-id="e3a04-281">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span> <span data-ttu-id="e3a04-282">Se o parâmetro callback retornar um valor, esse valor também se tornará o valor de retorno `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-282">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>

#### <span data-ttu-id="e3a04-283">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-283">Example</span></span>

```javascript
var user = Windows.System.UserProfile.UserInformation;

MSApp.execAtPriority(function () { // This callback executes synchronously.
  user.getFirstNameAsync().then(function () { // Dispatches at high priority.
    return user.getLastNameAsync();
  }).done(function () { // Dispatches at high priority.
    // USEFUL CODE HERE
  });
}, MSApp.HIGH); // The second argument of the execAtPriority method.
```

### <span data-ttu-id="e3a04-284">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="e3a04-284">getCurrentPriority</span></span> 
<span data-ttu-id="e3a04-285">Retorna a prioridade contextual atual.</span><span class="sxs-lookup"><span data-stu-id="e3a04-285">Returns the current contextual priority.</span></span>

```javascript
var retval = MSApp.getCurrentPriority();
```

#### <span data-ttu-id="e3a04-286">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-286">Parameters</span></span>
<span data-ttu-id="e3a04-287">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="e3a04-287">None.</span></span> 

#### <span data-ttu-id="e3a04-288">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-288">Return value</span></span>
|<span data-ttu-id="e3a04-289">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-289">Type</span></span> | <span data-ttu-id="e3a04-290">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-290">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-291">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-291">DOMString</span></span> | <span data-ttu-id="e3a04-292">O valor de retorno é uma das cadeias de caracteres `MSApp.HIGH` , `MSApp.NORMAL` ou `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-292">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>

#### <span data-ttu-id="e3a04-293">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-293">Remarks</span></span>
<span data-ttu-id="e3a04-294">Esse método retorna a prioridade contextual atual (consulte [`MSApp Constants`](#msapp-constants) ), que pode ser alterada via `execAtPriority` and `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-294">This method returns the current contextual priority (see [`MSApp Constants`](#msapp-constants)), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>

#### <span data-ttu-id="e3a04-295">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-295">Example</span></span>

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### <span data-ttu-id="e3a04-296">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="e3a04-296">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="e3a04-297">API síncrona que foi preterida.</span><span class="sxs-lookup"><span data-stu-id="e3a04-297">Synchronous API that has been deprecated.</span></span> <span data-ttu-id="e3a04-298">Para o Windows 10, consulte `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-298">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span> <span data-ttu-id="e3a04-299">Para aplicativos do Windows 8 e do 8,1, consulte a entrada MSDN para [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="e3a04-299">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="e3a04-300">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="e3a04-300">getHtmlPrintDocumentSourceAsync</span></span>
<span data-ttu-id="e3a04-301">Retorna o conteúdo de origem que será impresso.</span><span class="sxs-lookup"><span data-stu-id="e3a04-301">Returns the source content that is to be printed.</span></span>

#### <span data-ttu-id="e3a04-302">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-302">Parameters</span></span>
`htmlDoc` <span data-ttu-id="e3a04-303">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-303">[in]</span></span>

|<span data-ttu-id="e3a04-304">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-304">Type</span></span> | <span data-ttu-id="e3a04-305">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-305">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-306">Documento</span><span class="sxs-lookup"><span data-stu-id="e3a04-306">Document</span></span> | <span data-ttu-id="e3a04-307">O documento HTML a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="e3a04-307">The HTML document to be printed.</span></span> <span data-ttu-id="e3a04-308">Pode ser o documento raiz, o documento em um iframe, um fragmento de documento ou um documento SVG.</span><span class="sxs-lookup"><span data-stu-id="e3a04-308">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span> <span data-ttu-id="e3a04-309">Lembre-se de que htmlDoc deve ser um documento, não um elemento.</span><span class="sxs-lookup"><span data-stu-id="e3a04-309">Be aware that htmlDoc must be a document, not an element.</span></span>

#### <span data-ttu-id="e3a04-310">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3a04-310">Example 1</span></span>

```javascript
var printTask = event.request.createPrintTask(title, function (args) {
                var deferral = args.getDeferral();
                var getPrintDocumentSourceAsync;
                if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                    getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
                } else {
                    getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
                }
                getPrintDocumentSourceAsync.then(function (source) {
                    args.setSource(source);
                    deferral.complete();
                }, function (error) {
                    console.error(error);
                    deferral.complete();
                });
            });
```

#### <span data-ttu-id="e3a04-311">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e3a04-311">Example 2</span></span>

```javascript
    function registerForPrintContract() {
            var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
            printManager.onprinttaskrequested = onPrintTaskRequested;
            console.log("Print Contract registered. Use the Print button to print.", "sample", "status");
    }
    
    // Variable to hold the document source to print
    var gHtmlPrintDocumentSource = null;
    
    // Print event handler for printing via the PrintManager API.
    function onPrintTaskRequested(printEvent) {
        var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
            args.setSource(gHtmlPrintDocumentSource);
    
            // Register the handler for print task completion event
            printTask.oncompleted = onPrintTaskCompleted;
        });
    }
    
    // Print Task event handler is invoked when the print job is completed.
    function onPrintTaskCompleted(printTaskCompletionEvent) {
        // Notify the user about the failure
        if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
            console.log("Failed to print.", "sample", "error");
        }
    }
    
    // Executed just before printing.
    var beforePrint = function () {
        // Replace with code to be executed just before printing the current document:
    };
    
    // Executed immediately after printing.
    var afterPrint = function () {
        // Replace with code to be executed immediately after printing the current document:
    };
    
    function printButtonHandler() {
        // Optionally, functions to be executed immediately before and after printing can be configured as following:
        window.document.body.onbeforeprint = beforePrint;
        window.document.body.onafterprint = afterPrint;
    
        // Get document source to print
        MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
            gHtmlPrintDocumentSource = htmlPrintDocumentSource;
    
            // If the print contract is registered, the print experience is invoked.
            Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
        });
    }
```

### <span data-ttu-id="e3a04-312">getviewid</span><span class="sxs-lookup"><span data-stu-id="e3a04-312">getViewId</span></span> 
<span data-ttu-id="e3a04-313">Suporte para várias janelas.</span><span class="sxs-lookup"><span data-stu-id="e3a04-313">Support for multiple windows.</span></span> 

> [!NOTE] 
> <span data-ttu-id="e3a04-314">Nos aplicativos UWP do JavaScript do Win 8.1, há suporte para várias janelas usando APIs DOM do MSApp que agora são depricated.</span><span class="sxs-lookup"><span data-stu-id="e3a04-314">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span> <span data-ttu-id="e3a04-315">Para Windows 10, use `window.open` , `window` e o novo `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-315">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>

| <span data-ttu-id="e3a04-316">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-316">Description</span></span> |<span data-ttu-id="e3a04-317">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e3a04-317">Windows 10</span></span> | <span data-ttu-id="e3a04-318">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e3a04-318">Windows 8.1</span></span> |  
|:---- |:---- |:--- |  
| <span data-ttu-id="e3a04-319">Criar nova janela</span><span class="sxs-lookup"><span data-stu-id="e3a04-319">Create new window</span></span> | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|<span data-ttu-id="e3a04-320">Novo objeto Window</span><span class="sxs-lookup"><span data-stu-id="e3a04-320">New window object</span></span> | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### <span data-ttu-id="e3a04-321">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-321">Parameters</span></span>
`window`

|<span data-ttu-id="e3a04-322">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-322">Type</span></span> | <span data-ttu-id="e3a04-323">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-323">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-324">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-324">DOMString</span></span> | <span data-ttu-id="e3a04-325">Um objeto que representa uma janela que contém um documento DOM.</span><span class="sxs-lookup"><span data-stu-id="e3a04-325">An object representing a window containing a DOM document.</span></span> | 

#### <span data-ttu-id="e3a04-326">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-326">Return value</span></span>

`viewId`

|<span data-ttu-id="e3a04-327">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-327">Type</span></span> | <span data-ttu-id="e3a04-328">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-328">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-329">Número</span><span class="sxs-lookup"><span data-stu-id="e3a04-329">Number</span></span> | <span data-ttu-id="e3a04-330">Pode ser usado com várias [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span><span class="sxs-lookup"><span data-stu-id="e3a04-330">Can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

#### <span data-ttu-id="e3a04-331">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-331">Remarks</span></span>
<span data-ttu-id="e3a04-332">Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) e [`window`](https://developer.mozilla.org/docs/Web/API/Window) para criar novas janelas, mas então para interagir com APIs do WinRT, adicione a `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="e3a04-332">Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) and [`window`](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span> <span data-ttu-id="e3a04-333">Ele leva um `window` objeto como um parâmetro e retorna um `viewId` número que pode ser usado com várias [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span><span class="sxs-lookup"><span data-stu-id="e3a04-333">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

##### <span data-ttu-id="e3a04-334">Atraso na visibilidade</span><span class="sxs-lookup"><span data-stu-id="e3a04-334">Delaying Visibility</span></span> 
<span data-ttu-id="e3a04-335">Os modos de exibição do WinRT normalmente são iniciados e o desenvolvedor final usa algo como `TryShowAsStandaloneAsync` para exibir o modo de exibição quando ele está totalmente preparado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-335">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span> <span data-ttu-id="e3a04-336">No mundo da Web, `window.open` mostra uma janela imediatamente e o usuário final pode assistir à medida que o conteúdo é carregado e renderizado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-336">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span> <span data-ttu-id="e3a04-337">Para que seus novos modos de exibição do Windows atuem como modos de exibição no WinRT e não sejam exibidos imediatamente, adicionamos uma `window.open` opção.</span><span class="sxs-lookup"><span data-stu-id="e3a04-337">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span> <span data-ttu-id="e3a04-338">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e3a04-338">For example:</span></span>
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### <span data-ttu-id="e3a04-339">Diferenças da janela principal</span><span class="sxs-lookup"><span data-stu-id="e3a04-339">Primary Window Differences</span></span>
<span data-ttu-id="e3a04-340">A janela principal que é aberta inicialmente pelo sistema operacional funciona de forma diferente das janelas secundárias que ele abre:</span><span class="sxs-lookup"><span data-stu-id="e3a04-340">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span> 

|<span data-ttu-id="e3a04-341">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-341">Description</span></span> | <span data-ttu-id="e3a04-342">Primário</span><span class="sxs-lookup"><span data-stu-id="e3a04-342">Primary</span></span> | <span data-ttu-id="e3a04-343">Secundária</span><span class="sxs-lookup"><span data-stu-id="e3a04-343">Secondary</span></span> |
|:---- |:--- |:--- |
|<span data-ttu-id="e3a04-344">Window. Open</span><span class="sxs-lookup"><span data-stu-id="e3a04-344">window.open</span></span> | <span data-ttu-id="e3a04-345">Permitido</span><span class="sxs-lookup"><span data-stu-id="e3a04-345">Allowed</span></span> | <span data-ttu-id="e3a04-346">Não permitido</span><span class="sxs-lookup"><span data-stu-id="e3a04-346">Disallowed</span></span> |
|<span data-ttu-id="e3a04-347">Window. Close</span><span class="sxs-lookup"><span data-stu-id="e3a04-347">window.close</span></span> | <span data-ttu-id="e3a04-348">Fechar aplicativo</span><span class="sxs-lookup"><span data-stu-id="e3a04-348">Close app</span></span> | <span data-ttu-id="e3a04-349">Fechar a janela</span><span class="sxs-lookup"><span data-stu-id="e3a04-349">Close window</span></span> |
| <span data-ttu-id="e3a04-350">Restrições de navegação</span><span class="sxs-lookup"><span data-stu-id="e3a04-350">Navigation restrictions</span></span> | <span data-ttu-id="e3a04-351">ACUR apenas</span><span class="sxs-lookup"><span data-stu-id="e3a04-351">ACUR only</span></span> | <span data-ttu-id="e3a04-352">Sem restrições</span><span class="sxs-lookup"><span data-stu-id="e3a04-352">No restrictions</span></span> |

<span data-ttu-id="e3a04-353">A restrição para não permitir que janelas secundárias abertas pode mudar no futuro, dependendo do [Comentário](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span><span class="sxs-lookup"><span data-stu-id="e3a04-353">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>

##### <span data-ttu-id="e3a04-354">Restrições de comunicação de mesma origem</span><span class="sxs-lookup"><span data-stu-id="e3a04-354">Same Origin Communication Restrictions</span></span> 
<span data-ttu-id="e3a04-355">Há um problema técnico difícil que impede o suporte adequado a chamadas síncronas de mesma origem, de janela cruzada e de script.</span><span class="sxs-lookup"><span data-stu-id="e3a04-355">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span> <span data-ttu-id="e3a04-356">Quando você abre uma janela que é mesma origem, o script em uma janela tem permissão para chamar as funções diretamente na outra janela, e algumas dessas chamadas falharão.</span><span class="sxs-lookup"><span data-stu-id="e3a04-356">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span> `postMessage` <span data-ttu-id="e3a04-357">as chamadas funcionam muito bem e são a maneira recomendada de fazer coisas, se possível.</span><span class="sxs-lookup"><span data-stu-id="e3a04-357">calls work just fine and is the recommended way to do things if possible.</span></span> <span data-ttu-id="e3a04-358">O trabalho para melhorar esse problema está em andamento.</span><span class="sxs-lookup"><span data-stu-id="e3a04-358">Work to improve this issue is in progress.</span></span>


### <span data-ttu-id="e3a04-359">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="e3a04-359">isTaskScheduledAtPriorityOrHigher</span></span> 
<span data-ttu-id="e3a04-360">Retorna um valor booliano que indica se há trabalho pendente no nível de prioridade fornecido ou superior.</span><span class="sxs-lookup"><span data-stu-id="e3a04-360">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### <span data-ttu-id="e3a04-361">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-361">Parameters</span></span>
`priority` <span data-ttu-id="e3a04-362">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-362">[in]</span></span>

|<span data-ttu-id="e3a04-363">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-363">Type</span></span> | <span data-ttu-id="e3a04-364">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-364">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-365">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-365">DOMString</span></span> | <span data-ttu-id="e3a04-366">Um valor de prioridade (consulte [constantes MSApp](#msapp-constants)) especificando o nível de prioridade e acima para consultar qualquer trabalho pendente na fila.</span><span class="sxs-lookup"><span data-stu-id="e3a04-366">A priority value (see [MSApp Constants](#msapp-constants)) specifying the priority level and above to query for any outstanding queued work.</span></span>

#### <span data-ttu-id="e3a04-367">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-367">Return value</span></span>
|<span data-ttu-id="e3a04-368">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-368">Type</span></span> | <span data-ttu-id="e3a04-369">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-369">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-370">Booliano</span><span class="sxs-lookup"><span data-stu-id="e3a04-370">Boolean</span></span> | <span data-ttu-id="e3a04-371">Retorna `true` se houver algum trabalho em fila no nível de prioridade especificado ou acima, `false` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e3a04-371">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>

#### <span data-ttu-id="e3a04-372">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-372">Remarks</span></span>
<span data-ttu-id="e3a04-373">O `isTaskScheduledAtPriorityOrHigher` método fornece um meio para o código JavaScript determinar se há trabalho pendente nos vários níveis de prioridade (ou acima), com a intenção de que o código JavaScript de chamada possa decidir gerar um trabalho de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="e3a04-373">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels (or above) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>

#### <span data-ttu-id="e3a04-374">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-374">Example</span></span>

```javascript
function performIdleWork(array_in) {
  var idx = 0;

  function performIdleWorkHelper() {
    for (; idx < array_in.length; ++idx) {

      // USEFUL CODE HERE 

      if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
        MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
        break;
      } // if
    } // for
  } // performIdleWorkHelper

  performIdleWorkHelper();
} // performIdleWork
```

### <span data-ttu-id="e3a04-375">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="e3a04-375">pageHandlesAllApplicationActivations</span></span>
<span data-ttu-id="e3a04-376">Usado para evitar uma atualização do caminho inicial (recarregamento de página) antes de cada evento de ativação (IE. clique em uma notificação ou em um bloco fixado).</span><span class="sxs-lookup"><span data-stu-id="e3a04-376">Used to avoid a refresh of the start path (page reload) before every activate event (ie. clicking a notification or a pinned tile).</span></span> 

#### <span data-ttu-id="e3a04-377">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-377">Parameters</span></span>

|<span data-ttu-id="e3a04-378">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-378">Type</span></span> | <span data-ttu-id="e3a04-379">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-379">Description</span></span> |
|:---- |:--- |
<span data-ttu-id="e3a04-380">Booliano</span><span class="sxs-lookup"><span data-stu-id="e3a04-380">Boolean</span></span> | <span data-ttu-id="e3a04-381">Use `MSApp.pageHandlesAllApplicationActivations(true)` para sempre ignorar a atualização do caminho de início (recarregar página) e, em vez disso, saltar diretamente para acionar o `WebUIApplication` evento ativado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-381">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span> <span data-ttu-id="e3a04-382">Requer que todas as páginas manipulem eventos de ativação separadamente.</span><span class="sxs-lookup"><span data-stu-id="e3a04-382">Requires that all pages handle activation events separately.</span></span> <span data-ttu-id="e3a04-383">Ao definir esse método como `true` , clicar em um evento ativado (como um notificaiton) não disparará o recarregamento, um essencial para aplicativos de uma única página que desejam evitar recarregamentos de página.</span><span class="sxs-lookup"><span data-stu-id="e3a04-383">By defining this method as `true`, clicking an activated event (like a notificaiton) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>

#### <span data-ttu-id="e3a04-384">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-384">Example</span></span> 

```javascript
// Without this, the app will first refresh to the start path before every activate event
window.MSApp.pageHandlesAllApplicationActivations(true); 

// This must not be deffered so that it can receive the initial `activated` event in time
window.Windows.UI.WebUI.WebUIApplication.addEventListener(
    `activated`,
    e =>
        microsoftInterface.handleActivatedEvent(e);
    }),
    false
);
```

### <span data-ttu-id="e3a04-385">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="e3a04-385">suppressSubdownloadCredentialPrompts</span></span> 
<span data-ttu-id="e3a04-386">Controla se um aplicativo suprime possíveis prompts de autenticação durante o download de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3a04-386">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### <span data-ttu-id="e3a04-387">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-387">Parameters</span></span>
`suppress` <span data-ttu-id="e3a04-388">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-388">[in]</span></span>

|<span data-ttu-id="e3a04-389">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-389">Type</span></span> | <span data-ttu-id="e3a04-390">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-390">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-391">Booliano</span><span class="sxs-lookup"><span data-stu-id="e3a04-391">Boolean</span></span> | <span data-ttu-id="e3a04-392">Um valor de true suprime os prompts de autenticação potencial.</span><span class="sxs-lookup"><span data-stu-id="e3a04-392">A value of true suppresses potential authentication prompts.</span></span> <span data-ttu-id="e3a04-393">Um valor false não elimina qualquer prompt de autenticação potencial do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3a04-393">A value of false does not suppress any potential authentication prompts from the user.</span></span>

#### <span data-ttu-id="e3a04-394">Valor de Returan</span><span class="sxs-lookup"><span data-stu-id="e3a04-394">Returan value</span></span>
<span data-ttu-id="e3a04-395">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="e3a04-395">None.</span></span>

#### <span data-ttu-id="e3a04-396">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-396">Remarks</span></span>
<span data-ttu-id="e3a04-397">O `suppressSubdownloadCredentialPrompts` método controla se um aplicativo suprime solicitações de autenticação potenciais durante o download de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3a04-397">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span> <span data-ttu-id="e3a04-398">O comportamento padrão é não suprimir avisos de credenciais.</span><span class="sxs-lookup"><span data-stu-id="e3a04-398">The default behavior is to not suppress credential prompts.</span></span>

`suppressSubdownloadCredentialPrompts` <span data-ttu-id="e3a04-399">destina-se ao uso por aplicativos que podem carregar um número excessivo de recursos que exigem autenticação, como um aplicativo de email (que pode conter um boletim informativo contendo várias imagens em que cada imagem requer autenticação).</span><span class="sxs-lookup"><span data-stu-id="e3a04-399">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app (which could contain a newsletter containing a number of images where each image requires authentication).</span></span>

<span data-ttu-id="e3a04-400">Ao suprimir avisos de credenciais, as caixas de diálogo para autenticação em servidores não serão mostradas ao acessar recursos que exigem autenticação, e o recurso não será baixado.</span><span class="sxs-lookup"><span data-stu-id="e3a04-400">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span> <span data-ttu-id="e3a04-401">Observe que `suppressSubdownloadCredentialPrompts` não afeta outros prompts possíveis, como autenticação de proxy ou solicitação de certificação de cliente, nem afeta o XHR.</span><span class="sxs-lookup"><span data-stu-id="e3a04-401">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>

<span data-ttu-id="e3a04-402">Lembre-se de que `suppressSubdownloadCredentialPrompts` impacta todo o conteúdo do aplicativo, incluindo o conteúdo hospedado no `webview` elemento.</span><span class="sxs-lookup"><span data-stu-id="e3a04-402">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>
 
<span data-ttu-id="e3a04-403">**Importante:**  As decisões do prompt de credenciais são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="e3a04-403">**Important:**  Credential prompt decisions are cached.</span></span> <span data-ttu-id="e3a04-404">Portanto, ao suprimir as solicitações de credenciais entrarão em vigor imediatamente, permitir solicitações de credenciais após supressão delas poderá precisar de um recarregamento do documento para entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="e3a04-404">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>

#### <span data-ttu-id="e3a04-405">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-405">Example</span></span>

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### <span data-ttu-id="e3a04-406">terminateApp</span><span class="sxs-lookup"><span data-stu-id="e3a04-406">terminateApp</span></span>
<span data-ttu-id="e3a04-407">Termina o aplicativo atual e gera um relatório de falhas.</span><span class="sxs-lookup"><span data-stu-id="e3a04-407">Terminates the current application and generates a failure report.</span></span> 

```javascript
MSApp.terminateApp(error); 
```

#### <span data-ttu-id="e3a04-408">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-408">Parameters</span></span>
`error` <span data-ttu-id="e3a04-409">no</span><span class="sxs-lookup"><span data-stu-id="e3a04-409">[in]</span></span>

<span data-ttu-id="e3a04-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-410">Type</span></span> | <span data-ttu-id="e3a04-411">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-411">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-412">Erro</span><span class="sxs-lookup"><span data-stu-id="e3a04-412">Error</span></span> | <span data-ttu-id="e3a04-413">Um `Error` objeto que você pode usar para descrever o erro que disparou o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="e3a04-413">An `Error` object that you can use to describe the error that triggered the termination.</span></span> <span data-ttu-id="e3a04-414">O `Error` objeto deve conter as propriedades Number, Description e Stack; um relatório de falha não será gerado se o objeto não contiver essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e3a04-414">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>

#### <span data-ttu-id="e3a04-415">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-415">Return value</span></span>
<span data-ttu-id="e3a04-416">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="e3a04-416">None.</span></span>

#### <span data-ttu-id="e3a04-417">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3a04-417">Remarks</span></span>
<span data-ttu-id="e3a04-418">Se o problema relatado `terminateApp` se tornar um dos cinco principais problemas do seu aplicativo, ele será exibido na página de qualidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3a04-418">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>

#### <span data-ttu-id="e3a04-419">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-419">Example</span></span>
<span data-ttu-id="e3a04-420">Este exemplo chama `terminateApp` quando uma exceção é encontrada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-420">This example calls `terminateApp` when an exception is encountered.</span></span> <span data-ttu-id="e3a04-421">Ele usa o `Error` objeto fornecido quando você captura uma exceção.</span><span class="sxs-lookup"><span data-stu-id="e3a04-421">It uses the `Error` object provided when you catch an exception.</span></span> 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### <span data-ttu-id="e3a04-422">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="e3a04-422">MSApp Constants</span></span>
<span data-ttu-id="e3a04-423">Valores de prioridade permitidos associados a `execAsyncAtPriority` , `execAtPriority` , `getCurrentPriority` e `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-423">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>

#### <span data-ttu-id="e3a04-424">Atual</span><span class="sxs-lookup"><span data-stu-id="e3a04-424">Current</span></span>
`current`

|<span data-ttu-id="e3a04-425">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-425">Type</span></span> | <span data-ttu-id="e3a04-426">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-426">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-427">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-427">DOMString</span></span> | <span data-ttu-id="e3a04-428">Quando `current` usado com o método apropriado (consulte também a seção), o método usará a prioridade contextual atual ao executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-428">When `current` is used with the appropriate method (See also section), the method will use the current contextual priority when executing the requested operation.</span></span>

#### <span data-ttu-id="e3a04-429">Alto</span><span class="sxs-lookup"><span data-stu-id="e3a04-429">High</span></span>
`high`

|<span data-ttu-id="e3a04-430">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-430">Type</span></span> | <span data-ttu-id="e3a04-431">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-431">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-432">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-432">DOMString</span></span> | <span data-ttu-id="e3a04-433">Quando `high` usado com o método apropriado (consulte também a seção), o método usará maior prioridade normal ao executar a operação solicitada e enviará a operação antes de qualquer trabalho normal de prioridade existente.</span><span class="sxs-lookup"><span data-stu-id="e3a04-433">When `high` is used with the appropriate method (See also section), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>

#### <span data-ttu-id="e3a04-434">Ocioso</span><span class="sxs-lookup"><span data-stu-id="e3a04-434">Idle</span></span>
`idle`

|<span data-ttu-id="e3a04-435">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-435">Type</span></span> | <span data-ttu-id="e3a04-436">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-436">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-437">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-437">DOMString</span></span> | <span data-ttu-id="e3a04-438">Quando `ideal` é usado com o método apropriado (consulte também a seção), o método usará a prioridade mais baixa do que o normal ao executar a operação solicitada e enviará a operação após qualquer trabalho normal de prioridade existente.</span><span class="sxs-lookup"><span data-stu-id="e3a04-438">When `ideal` is used with the appropriate method (See also section), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>

#### <span data-ttu-id="e3a04-439">Normal</span><span class="sxs-lookup"><span data-stu-id="e3a04-439">Normal</span></span>
`normal`

|<span data-ttu-id="e3a04-440">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-440">Type</span></span> | <span data-ttu-id="e3a04-441">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-441">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-442">DOMString</span><span class="sxs-lookup"><span data-stu-id="e3a04-442">DOMString</span></span> | <span data-ttu-id="e3a04-443">Quando `normal` usado com o método apropriado (consulte também a seção), o método usará a prioridade existente normal ao executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="e3a04-443">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>

#### <span data-ttu-id="e3a04-444">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3a04-444">Example</span></span>

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### <span data-ttu-id="e3a04-445">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a04-445">Requirements</span></span>
|<span data-ttu-id="e3a04-446">IDL</span><span class="sxs-lookup"><span data-stu-id="e3a04-446">IDL</span></span> | <span data-ttu-id="e3a04-447">Mshtml. idl</span><span class="sxs-lookup"><span data-stu-id="e3a04-447">Mshtml.idl</span></span> |
|:---- |:--- |

## <span data-ttu-id="e3a04-448">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="e3a04-448">MSAppAsyncOperation</span></span>

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### <span data-ttu-id="e3a04-449">start</span><span class="sxs-lookup"><span data-stu-id="e3a04-449">start</span></span>
<span data-ttu-id="e3a04-450">Inicia o `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-450">Starts the `MSAppAsyncOperation`.</span></span>

```javascript
var retval = MSAppAsyncOperation.start();
```

#### <span data-ttu-id="e3a04-451">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3a04-451">Parameters</span></span>
<span data-ttu-id="e3a04-452">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="e3a04-452">None.</span></span>

#### <span data-ttu-id="e3a04-453">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e3a04-453">Return value</span></span>
<span data-ttu-id="e3a04-454">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="e3a04-454">None.</span></span>

#### <span data-ttu-id="e3a04-455">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e3a04-455">Properties</span></span>
`error` <span data-ttu-id="e3a04-456">folha</span><span class="sxs-lookup"><span data-stu-id="e3a04-456">property</span></span>

|<span data-ttu-id="e3a04-457">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-457">Type</span></span> | <span data-ttu-id="e3a04-458">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-458">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-459">DOMError</span><span class="sxs-lookup"><span data-stu-id="e3a04-459">DOMError</span></span> | <span data-ttu-id="e3a04-460">Representa um erro em `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-460">Represents an error in `MSAppAsyncOperation`.</span></span>

```javascript
p = object.error
```

`oncomplete` <span data-ttu-id="e3a04-461">folha</span><span class="sxs-lookup"><span data-stu-id="e3a04-461">property</span></span>

|<span data-ttu-id="e3a04-462">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-462">Type</span></span> | <span data-ttu-id="e3a04-463">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-463">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-464">EventHandler</span><span class="sxs-lookup"><span data-stu-id="e3a04-464">EventHandler</span></span> | <span data-ttu-id="e3a04-465">Propriedade para definir um manipulador de eventos na conclusão de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-465">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.oncomplete
```

`onerror` <span data-ttu-id="e3a04-466">folha</span><span class="sxs-lookup"><span data-stu-id="e3a04-466">property</span></span>

|<span data-ttu-id="e3a04-467">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-467">Type</span></span> | <span data-ttu-id="e3a04-468">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-468">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-469">EventHandler</span><span class="sxs-lookup"><span data-stu-id="e3a04-469">EventHandler</span></span> | <span data-ttu-id="e3a04-470">Propriedade para definir um manipulador de eventos em um erro durante `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-470">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>

```javascript
p = object.onerror
```

`readyState` <span data-ttu-id="e3a04-471">folha</span><span class="sxs-lookup"><span data-stu-id="e3a04-471">property</span></span>

|<span data-ttu-id="e3a04-472">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-472">Type</span></span> | <span data-ttu-id="e3a04-473">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-473">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-474">Número</span><span class="sxs-lookup"><span data-stu-id="e3a04-474">Number</span></span> | <span data-ttu-id="e3a04-475">Representa o estado da operação assíncrona dentro do aplicativo do Windows usando JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e3a04-475">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span> <span data-ttu-id="e3a04-476">Os valores incluem: iniciado [0], concluído [1], erro [2].</span><span class="sxs-lookup"><span data-stu-id="e3a04-476">Values include: Started[0], Completed[1], Error[2].</span></span>

```javascript
p = object.readyState
```

`result` <span data-ttu-id="e3a04-477">folha</span><span class="sxs-lookup"><span data-stu-id="e3a04-477">property</span></span>

|<span data-ttu-id="e3a04-478">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3a04-478">Type</span></span> | <span data-ttu-id="e3a04-479">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3a04-479">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="e3a04-480">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3a04-480">Any</span></span> |<span data-ttu-id="e3a04-481">Representa o resultado de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="e3a04-481">Represents the result of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.result
```
