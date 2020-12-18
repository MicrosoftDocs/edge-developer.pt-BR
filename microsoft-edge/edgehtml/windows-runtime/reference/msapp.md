---
title: Referência de API MSApp
description: Fornece funções auxiliares que permitem criar objetos BLOB e MSStream.  Os objetos e membros do MSApp têm suporte para aplicativos do Windows que usam JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carregamento de arquivo, blog, MSStream, aplicativos do Windows 10, UWP, Edge
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a3ad670f61bfafa4480c538dd8f28c7013b7d7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231542"
---
# <span data-ttu-id="b0da0-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="b0da0-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="b0da0-106">O objeto MSApp e seus membros têm suporte somente para aplicativos do Windows que usam JavaScript \ (incluindo PWAs acessando recursos da API do Windows \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="b0da0-107">O objeto MSApp existe somente no contexto local de um documento HTML em um aplicativo do Windows carregado por meio do esquema de URI MS-Appx; caso contrário, o objeto não existe (e conseqüentemente, nenhum de seus métodos e propriedades estão disponíveis).</span><span class="sxs-lookup"><span data-stu-id="b0da0-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="b0da0-108">Ele fornece funções auxiliares que permitem criar objetos [blob](https://developer.mozilla.org/docs/Web/API/Blob) e [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0da0-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="b0da0-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0da0-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b0da0-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getviewid](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="b0da0-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b0da0-111">:</span><span class="sxs-lookup"><span data-stu-id="b0da0-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b0da0-112">[atual](#current), [alto](#high), [ocioso](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="b0da0-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b0da0-113">Interface MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="b0da0-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="b0da0-114">start</span><span class="sxs-lookup"><span data-stu-id="b0da0-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="b0da0-115">Métodos MSApp</span><span class="sxs-lookup"><span data-stu-id="b0da0-115">MSApp methods</span></span>  

### <span data-ttu-id="b0da0-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="b0da0-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-117">Limpa o cache e os dados do indexedDB para o aplicativo ou [WebView](../../hosting/webview/index.md).</span><span class="sxs-lookup"><span data-stu-id="b0da0-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-118">Parameters</span></span>**  
      
      <span data-ttu-id="b0da0-119">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b0da0-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-120">Return value</span></span>**  
      
      <span data-ttu-id="b0da0-121">Tipo: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="b0da0-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="b0da0-122">Representa uma ação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b0da0-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-123">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-123">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-124">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-125">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-126">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="b0da0-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-129">Cria um [blob](https://developer.mozilla.org/docs/Web/API/Blob) a partir de um objeto [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) .</span><span class="sxs-lookup"><span data-stu-id="b0da0-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="b0da0-130">Esse método deve ser usado ao lidar com `IRandomAccessStream` objetos em aplicativos para criar um objeto baseado no W3C a partir do Stream.</span><span class="sxs-lookup"><span data-stu-id="b0da0-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="b0da0-131">Depois que o blob é criado, ele pode ser usado com o [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [APIs de URL](https://developer.mozilla.org/docs/Web/API/URL)e [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="b0da0-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="b0da0-133">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-133">[in]</span></span>  
      
      | <span data-ttu-id="b0da0-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-134">Type</span></span> | <span data-ttu-id="b0da0-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-136">String</span><span class="sxs-lookup"><span data-stu-id="b0da0-136">String</span></span> | <span data-ttu-id="b0da0-137">Tipo de conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="b0da0-137">Content type of the data.</span></span>  <span data-ttu-id="b0da0-138">Essa cadeia de caracteres deve estar no formato especificado no token do tipo de mídia definido na seção 3,7 da RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="b0da0-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="b0da0-139">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-139">[in]</span></span>  
      
      | <span data-ttu-id="b0da0-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-140">Type</span></span> | <span data-ttu-id="b0da0-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-142">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-142">Any</span></span> | <span data-ttu-id="b0da0-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) a ser armazenado no BLOB.</span><span class="sxs-lookup"><span data-stu-id="b0da0-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-144">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-144">Return value</span></span>**  
      
      | <span data-ttu-id="b0da0-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-145">Type</span></span> | <span data-ttu-id="b0da0-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-147">Irregular</span><span class="sxs-lookup"><span data-stu-id="b0da0-147">Blob</span></span> | <span data-ttu-id="b0da0-148">Novo objeto BLOB que contém o fluxo.</span><span class="sxs-lookup"><span data-stu-id="b0da0-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-149">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="b0da0-150">Extremamente</span><span class="sxs-lookup"><span data-stu-id="b0da0-150">Exception</span></span> | <span data-ttu-id="b0da0-151">Condição</span><span class="sxs-lookup"><span data-stu-id="b0da0-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="b0da0-152">TypeMismatchError</span></span> | <span data-ttu-id="b0da0-153">O tipo de nó é incompatível com o tipo de parâmetro esperado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="b0da0-154">Para versões anteriores ao Internet Explorer 10, TYPE_MISMATCH_ERR é retornado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-155">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-156">Cria um blob a partir de tipos do Windows Runtime por meio do namespace MSApp no objeto Window.</span><span class="sxs-lookup"><span data-stu-id="b0da0-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="b0da0-157">Esse método criará um blob que é essencialmente um wrapper Light sobre o objeto [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) fornecido a ele.</span><span class="sxs-lookup"><span data-stu-id="b0da0-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="b0da0-158">O blob é proprietário do tempo de vida desse fluxo e o fluxo será fechado quando o blob for destruído.</span><span class="sxs-lookup"><span data-stu-id="b0da0-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-159">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-159">Example</span></span>**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="b0da0-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-161">Converte o intervalo especificado do usuário ou do aplicativo em um fragmento de HTML que pode ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-162">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="b0da0-163">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-163">[in]</span></span>  
      
      | <span data-ttu-id="b0da0-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-164">Type</span></span> | <span data-ttu-id="b0da0-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-166">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-166">Any</span></span> | <span data-ttu-id="b0da0-167">Esse intervalo pode ser criado a partir de um objeto Selection, por exemplo: `window.selection.getRangeAt(0)` ou manualmente.</span><span class="sxs-lookup"><span data-stu-id="b0da0-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-168">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-168">Return value</span></span>**  
      
      | <span data-ttu-id="b0da0-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-169">Type</span></span> | <span data-ttu-id="b0da0-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-171">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-171">Any</span></span> | <span data-ttu-id="b0da0-172">Contém a marcação HTML para o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-173">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-173">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-174">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-175">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-176">Esse método oferece suporte somente ao [intervalo dom](https://developer.mozilla.org/docs/Web/API/Range), e não a [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="b0da0-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="b0da0-177">O pacote de dados retornado para o intervalo especificado contém marcação HTML no formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="b0da0-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="b0da0-178">Não há propriedades disponíveis para o pacote de dados retornado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-179">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-179">Example</span></span>**  
      
      <span data-ttu-id="b0da0-180">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="b0da0-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-182">Converte a seleção do usuário ou do aplicativo em um fragmento HTML que pode ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-183">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-183">Parameters</span></span>**  
      
      <span data-ttu-id="b0da0-184">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b0da0-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-185">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-185">Return value</span></span>**  
      
      | <span data-ttu-id="b0da0-186">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-186">Type</span></span> | <span data-ttu-id="b0da0-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-188">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-188">Any</span></span> | <span data-ttu-id="b0da0-189">Contém a marcação HTML para o intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-190">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-190">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-191">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-192">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-192">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-193">O pacote de dados retornado para a seleção contém marcação HTML no formato da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="b0da0-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="b0da0-194">Se não houver nenhuma seleção de usuário em qualquer lugar dentro da interface do usuário do aplicativo, o `createDataPackageFromSelection` retorno será retornado `null` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="b0da0-195">Não há propriedades disponíveis para o pacote de dados retornado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-196">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <span data-ttu-id="b0da0-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="b0da0-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-198">Converte um [](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) WinRT em um objeto de [arquivo](https://developer.mozilla.org/docs/Web/API/File) W3C padrão.</span><span class="sxs-lookup"><span data-stu-id="b0da0-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-199">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="b0da0-200">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-200">[in]</span></span>
      
      | <span data-ttu-id="b0da0-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-201">Type</span></span> | <span data-ttu-id="b0da0-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-203">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-203">Any</span></span> | <span data-ttu-id="b0da0-204">Contém o arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b0da0-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-205">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-205">Return value</span></span>**
      
      <span data-ttu-id="b0da0-206">Nenhum(a)</span><span class="sxs-lookup"><span data-stu-id="b0da0-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-207">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="b0da0-208">Extremamente</span><span class="sxs-lookup"><span data-stu-id="b0da0-208">Exception</span></span> | <span data-ttu-id="b0da0-209">Condição</span><span class="sxs-lookup"><span data-stu-id="b0da0-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="b0da0-210">TypeMismatchError</span></span> | <span data-ttu-id="b0da0-211">A referência do arquivo W3C especificado é inválida.</span><span class="sxs-lookup"><span data-stu-id="b0da0-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="b0da0-212">Para versões anteriores ao Internet Explorer 10, `TYPE_MISMATCH_ERR` será retornada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-213">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-213">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-214">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-215">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="b0da0-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-217">Cria um [MSStream](https://msdn.microsoft.com/library/hh772328) de um [InputStream](https://msdn.microsoft.com/library/hh772327).</span><span class="sxs-lookup"><span data-stu-id="b0da0-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-218">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="b0da0-219">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-219">[in]</span></span>
      
      | <span data-ttu-id="b0da0-220">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-220">Type</span></span> | <span data-ttu-id="b0da0-221">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-222">DOMString</span></span> | <span data-ttu-id="b0da0-223">Tipo de conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="b0da0-223">Content type of the data.</span></span>  <span data-ttu-id="b0da0-224">Essa cadeia de caracteres deve estar no formato especificado no token do tipo de mídia definido na seção 3,7 da RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="b0da0-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="b0da0-225">\ ([Veja tipos MIME,] (como,,,,,,, https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` `text/html` `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` e assim por diante \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="b0da0-226">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-226">[in]</span></span>
      
      | <span data-ttu-id="b0da0-227">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-227">Type</span></span> | <span data-ttu-id="b0da0-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-229">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-229">Any</span></span> | <span data-ttu-id="b0da0-230">A [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) a ser armazenada no `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-231">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-231">Return value</span></span>**
      
      <span data-ttu-id="b0da0-232">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-233">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-233">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-234">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-235">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-235">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-236">Esse método assume um tipo de conteúdo e a `IInputStream` referência.</span><span class="sxs-lookup"><span data-stu-id="b0da0-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="b0da0-237">Em seguida, o método verifica se a referência do fluxo transmitida é uma instância do tipo `IInputStream` e, se não for, throws `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="b0da0-238">Se não ocorrerem erros, `createStreamFromInputStream` cria um `MSStream` \ (a partir de suas entradas \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-239">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-239">Example</span></span>**  
      
      <span data-ttu-id="b0da0-240">Um `IInputStream` pode ser usado para criar um `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="b0da0-241">Como `MSStreams` são objetos inerentemente de uso único, todas as URLs criadas por `URL.createObjectURL` são revogadas na primeira vez que são resolvidas pelo elemento Image.</span><span class="sxs-lookup"><span data-stu-id="b0da0-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="b0da0-242">Além disso, as solicitações para uma segunda URL neste objeto após o fluxo ter sido usado falharão.</span><span class="sxs-lookup"><span data-stu-id="b0da0-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="b0da0-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-244">Agenda um retorno de chamada para ser executado em um momento posterior, de acordo com a prioridade determinada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-245">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="b0da0-246">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-246">[in]</span></span>
      
      | <span data-ttu-id="b0da0-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-247">Type</span></span> | <span data-ttu-id="b0da0-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-249">Função</span><span class="sxs-lookup"><span data-stu-id="b0da0-249">Function</span></span> | <span data-ttu-id="b0da0-250">A função de retorno de chamada para ser executada de forma assíncrona, despachada com a prioridade determinada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="b0da0-251">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-251">[in]</span></span>
      
      | <span data-ttu-id="b0da0-252">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-252">Type</span></span> | <span data-ttu-id="b0da0-253">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-254">DOMString</span></span> | <span data-ttu-id="b0da0-255">O valor de prioridade contextual no qual o retorno de chamada do asynchronousCallback é executado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="b0da0-256">Consulte [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="b0da0-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="b0da0-257">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-257">[in]</span></span>
      
      | <span data-ttu-id="b0da0-258">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-258">Type</span></span> | <span data-ttu-id="b0da0-259">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="b0da0-260">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-260">Any</span></span> | <span data-ttu-id="b0da0-261">Uma série opcional de argumentos que são passados para a função de retorno de chamada synchronousCallback \ (como parâmetros 1 e assim por diante \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-262">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-262">Return value</span></span>**  
      
      <span data-ttu-id="b0da0-263">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b0da0-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-264">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-264">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-265">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-266">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-266">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-267">A `asynchronousCallback` função de retorno de chamada fornecida será executada de forma assíncrona mais tarde.</span><span class="sxs-lookup"><span data-stu-id="b0da0-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="b0da0-268">será despachado de acordo com a prioridade fornecida.</span><span class="sxs-lookup"><span data-stu-id="b0da0-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="b0da0-269">A prioridade normal é equivalente ao método [setimmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existente.</span><span class="sxs-lookup"><span data-stu-id="b0da0-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="b0da0-270">Quando o retorno de chamada é executado, a prioridade contextual atual é definida como o valor de parâmetro de prioridade fornecido para a duração da execução do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="b0da0-271">O `asynchronousCallback` parâmetro callback pode ser qualquer função.</span><span class="sxs-lookup"><span data-stu-id="b0da0-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="b0da0-272">Se os argumentos forem fornecidos após o `priority` parâmetro, todos serão passados para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="b0da0-273">Ao contrário `execAtPriority` , qualquer objeto retornado pela `asynchronousCallback` função de retorno de chamada é ignorado \ (e não retornado via `execAsyncAtPriority` \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-274">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="b0da0-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-276">Executa a função de retorno de chamada especificada na prioridade contextual determinada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-277">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="b0da0-278">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-278">[in]</span></span>  
      
      | <span data-ttu-id="b0da0-279">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-279">Type</span></span> | <span data-ttu-id="b0da0-280">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-281">Função</span><span class="sxs-lookup"><span data-stu-id="b0da0-281">Function</span></span> | <span data-ttu-id="b0da0-282">A função de retorno de chamada a ser executada de forma síncrona na prioridade contextual determinada prioridade.</span><span class="sxs-lookup"><span data-stu-id="b0da0-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="b0da0-283">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-283">[in]</span></span>  
      
      | <span data-ttu-id="b0da0-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-284">Type</span></span> | <span data-ttu-id="b0da0-285">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-286">DOMString</span></span> | <span data-ttu-id="b0da0-287">O valor de prioridade especificado ao qual o valor de prioridade contextual atual será definido ao executar a `synchronousCallback` função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="b0da0-288">Consulte [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="b0da0-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="b0da0-289">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-289">[in]</span></span>  
      
      | <span data-ttu-id="b0da0-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-290">Type</span></span> | <span data-ttu-id="b0da0-291">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-292">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-292">Any</span></span> | <span data-ttu-id="b0da0-293">Uma série opcional de argumentos que são passados para a `synchronousCallback` função de retorno de chamada \ (como parâmetros 1 e assim por diante \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-294">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-294">Return value</span></span>**  
      
      | <span data-ttu-id="b0da0-295">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-295">Type</span></span> | <span data-ttu-id="b0da0-296">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-297">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-297">Any</span></span> | <span data-ttu-id="b0da0-298">Retorna o valor de retorno do `synchronousCallback` retorno de chamada \ (conforme aplicável \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-299">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-299">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-300">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-301">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-301">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-302">O `synchronousCallback` método callback fornecido é executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="b0da0-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="b0da0-303">A prioridade contextual atual é alterada para o valor de prioridade fornecido (fornecido pelo argumento Priority) para a duração da função de retorno de chamada fornecida.</span><span class="sxs-lookup"><span data-stu-id="b0da0-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="b0da0-304">Depois que a execução da função de retorno de chamada terminar, a prioridade será retornada ao valor anterior antes da `execAtPriority` chamada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="b0da0-305">O valor de retorno `execAtPriority` é o valor de retorno do método callback \ (conforme fornecido \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="b0da0-306">O `synchronousCallback` parâmetro callback pode ser qualquer função.</span><span class="sxs-lookup"><span data-stu-id="b0da0-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="b0da0-307">Se algum argumento for fornecido após o parâmetro Priority, ele será passado para o método callback fornecido.</span><span class="sxs-lookup"><span data-stu-id="b0da0-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="b0da0-308">Se o parâmetro callback retornar um valor, esse valor também se tornará o valor de retorno `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-309">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-309">Example</span></span>**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="b0da0-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-311">Retorna a prioridade contextual atual.</span><span class="sxs-lookup"><span data-stu-id="b0da0-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-312">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-312">Parameters</span></span>**  
      
      <span data-ttu-id="b0da0-313">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-314">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-314">Return value</span></span>**  
      
      | <span data-ttu-id="b0da0-315">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-315">Type</span></span> | <span data-ttu-id="b0da0-316">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-317">DOMString</span></span> | <span data-ttu-id="b0da0-318">O valor de retorno é uma das cadeias de caracteres `MSApp.HIGH` , `MSApp.NORMAL` ou `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-319">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-319">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-320">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-321">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-321">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-322">Esse método retorna a prioridade contextual atual \ (consulte as [constantes MSApp](#msapp-constants)\), que podem ser alteradas via `execAtPriority` e `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-323">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-323">Example</span></span>**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="b0da0-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="b0da0-325">API síncrona que foi preterida.</span><span class="sxs-lookup"><span data-stu-id="b0da0-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="b0da0-326">Para o Windows 10, consulte `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="b0da0-327">Para aplicativos do Windows 8 e do 8,1, consulte a entrada MSDN para [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="b0da0-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="b0da0-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="b0da0-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-329">Retorna o conteúdo de origem que será impresso.</span><span class="sxs-lookup"><span data-stu-id="b0da0-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-330">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="b0da0-331">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-331">[in]</span></span>  
      
      | <span data-ttu-id="b0da0-332">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-332">Type</span></span> | <span data-ttu-id="b0da0-333">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-334">Documento</span><span class="sxs-lookup"><span data-stu-id="b0da0-334">Document</span></span> | <span data-ttu-id="b0da0-335">O documento HTML a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="b0da0-335">The HTML document to be printed.</span></span>  <span data-ttu-id="b0da0-336">Pode ser o documento raiz, o documento em um iframe, um fragmento de documento ou um documento SVG.</span><span class="sxs-lookup"><span data-stu-id="b0da0-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="b0da0-337">Lembre-se de que htmlDoc deve ser um documento, não um elemento.</span><span class="sxs-lookup"><span data-stu-id="b0da0-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-338">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-338">Return value</span></span>**
      
      <span data-ttu-id="b0da0-339">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-340">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-340">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-341">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-342">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-342">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-343">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-344">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b0da0-344">Example 1</span></span>**  
      
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
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-345">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b0da0-345">Example 2</span></span>**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
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
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-346">getviewid</span><span class="sxs-lookup"><span data-stu-id="b0da0-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-347">Suporte para várias janelas.</span><span class="sxs-lookup"><span data-stu-id="b0da0-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="b0da0-348">Nos aplicativos UWP do JavaScript do Win 8.1, há suporte para várias janelas usando APIs DOM do MSApp que agora são depricated.</span><span class="sxs-lookup"><span data-stu-id="b0da0-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="b0da0-349">Para Windows 10, use `window.open` , `window` e o novo `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="b0da0-350">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-350">Description</span></span> |<span data-ttu-id="b0da0-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b0da0-351">Windows 10</span></span> | <span data-ttu-id="b0da0-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b0da0-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="b0da0-353">Criar nova janela</span><span class="sxs-lookup"><span data-stu-id="b0da0-353">Create new window</span></span> | [<span data-ttu-id="b0da0-354">Window. Open</span><span class="sxs-lookup"><span data-stu-id="b0da0-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="b0da0-355">MSApp. createNewView</span><span class="sxs-lookup"><span data-stu-id="b0da0-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="b0da0-356">Novo objeto Window</span><span class="sxs-lookup"><span data-stu-id="b0da0-356">New window object</span></span> | [<span data-ttu-id="b0da0-357">janela</span><span class="sxs-lookup"><span data-stu-id="b0da0-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="b0da0-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="b0da0-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-359">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="b0da0-360">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-360">Type</span></span> | <span data-ttu-id="b0da0-361">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-362">DOMString</span></span> | <span data-ttu-id="b0da0-363">Um objeto que representa uma janela que contém um documento DOM.</span><span class="sxs-lookup"><span data-stu-id="b0da0-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-364">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="b0da0-365">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-365">Type</span></span> | <span data-ttu-id="b0da0-366">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-367">Número</span><span class="sxs-lookup"><span data-stu-id="b0da0-367">Number</span></span> | <span data-ttu-id="b0da0-368">Pode ser usado com várias APIs [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="b0da0-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-369">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-369">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-370">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-371">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-371">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-372">Use [Window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) e [Window](https://developer.mozilla.org/docs/Web/API/Window) para criar novas janelas, mas então para interagir com APIs do WinRT, adicione a `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="b0da0-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="b0da0-373">Ele leva um `window` objeto como um parâmetro e retorna um `viewId` número que pode ser usado com as várias APIs [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="b0da0-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="b0da0-374">Atraso na visibilidade</span><span class="sxs-lookup"><span data-stu-id="b0da0-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="b0da0-375">Os modos de exibição do WinRT normalmente são iniciados e o desenvolvedor final usa algo como `TryShowAsStandaloneAsync` para exibir o modo de exibição quando ele está totalmente preparado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="b0da0-376">No mundo da Web, `window.open` mostra uma janela imediatamente e o usuário final pode assistir à medida que o conteúdo é carregado e renderizado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="b0da0-377">Para que seus novos modos de exibição do Windows atuem como modos de exibição no WinRT e não sejam exibidos imediatamente, adicionamos uma `window.open` opção.</span><span class="sxs-lookup"><span data-stu-id="b0da0-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="b0da0-378">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b0da0-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="b0da0-379">Diferenças da janela principal</span><span class="sxs-lookup"><span data-stu-id="b0da0-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="b0da0-380">A janela principal que é aberta inicialmente pelo sistema operacional funciona de forma diferente das janelas secundárias que ele abre:</span><span class="sxs-lookup"><span data-stu-id="b0da0-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="b0da0-381">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-381">Description</span></span> | <span data-ttu-id="b0da0-382">Primário</span><span class="sxs-lookup"><span data-stu-id="b0da0-382">Primary</span></span> | <span data-ttu-id="b0da0-383">Secundária</span><span class="sxs-lookup"><span data-stu-id="b0da0-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="b0da0-384">Window. Open</span><span class="sxs-lookup"><span data-stu-id="b0da0-384">window.open</span></span> | <span data-ttu-id="b0da0-385">Permitido</span><span class="sxs-lookup"><span data-stu-id="b0da0-385">Allowed</span></span> | <span data-ttu-id="b0da0-386">Não permitido</span><span class="sxs-lookup"><span data-stu-id="b0da0-386">Disallowed</span></span> |  
          | <span data-ttu-id="b0da0-387">Window. Close</span><span class="sxs-lookup"><span data-stu-id="b0da0-387">window.close</span></span> | <span data-ttu-id="b0da0-388">Fechar aplicativo</span><span class="sxs-lookup"><span data-stu-id="b0da0-388">Close app</span></span> | <span data-ttu-id="b0da0-389">Fechar a janela</span><span class="sxs-lookup"><span data-stu-id="b0da0-389">Close window</span></span> |  
          | <span data-ttu-id="b0da0-390">Restrições de navegação</span><span class="sxs-lookup"><span data-stu-id="b0da0-390">Navigation restrictions</span></span> | <span data-ttu-id="b0da0-391">ACUR apenas</span><span class="sxs-lookup"><span data-stu-id="b0da0-391">ACUR only</span></span> | <span data-ttu-id="b0da0-392">Sem restrições</span><span class="sxs-lookup"><span data-stu-id="b0da0-392">No restrictions</span></span> |  
          
          <span data-ttu-id="b0da0-393">A restrição para não permitir que janelas secundárias abertas pode mudar no futuro, dependendo do [Comentário](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span><span class="sxs-lookup"><span data-stu-id="b0da0-393">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>  
      
      *   <span data-ttu-id="b0da0-394">Restrições de comunicação de mesma origem</span><span class="sxs-lookup"><span data-stu-id="b0da0-394">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="b0da0-395">Há um problema técnico difícil que impede o suporte adequado a chamadas síncronas de mesma origem, de janela cruzada e de script.</span><span class="sxs-lookup"><span data-stu-id="b0da0-395">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="b0da0-396">Quando você abre uma janela que é mesma origem, o script em uma janela tem permissão para chamar as funções diretamente na outra janela, e algumas dessas chamadas falharão.</span><span class="sxs-lookup"><span data-stu-id="b0da0-396">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="b0da0-397">as chamadas funcionam muito bem e são a maneira recomendada de fazer coisas, se possível.</span><span class="sxs-lookup"><span data-stu-id="b0da0-397">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="b0da0-398">O trabalho para melhorar esse problema está em andamento.</span><span class="sxs-lookup"><span data-stu-id="b0da0-398">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-399">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-399">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <span data-ttu-id="b0da0-400">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="b0da0-400">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-401">Retorna um valor booliano que indica se há trabalho pendente no nível de prioridade fornecido ou superior.</span><span class="sxs-lookup"><span data-stu-id="b0da0-401">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-402">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-402">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="b0da0-403">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-403">[in]</span></span>
      
      | <span data-ttu-id="b0da0-404">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-404">Type</span></span> | <span data-ttu-id="b0da0-405">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-405">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-406">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-406">DOMString</span></span> | <span data-ttu-id="b0da0-407">Um valor de prioridade \ (consulte [constantes MSApp](#msapp-constants)\) especificando o nível de prioridade e acima para consultar qualquer trabalho em fila pendente.</span><span class="sxs-lookup"><span data-stu-id="b0da0-407">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-408">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-408">Return value</span></span>**  
      
      | <span data-ttu-id="b0da0-409">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-409">Type</span></span> | <span data-ttu-id="b0da0-410">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-410">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-411">Booliano</span><span class="sxs-lookup"><span data-stu-id="b0da0-411">Boolean</span></span> | <span data-ttu-id="b0da0-412">Retorna `true` se houver algum trabalho em fila no nível de prioridade especificado ou acima, `false` caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b0da0-412">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-413">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-413">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-414">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-414">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-415">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-415">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-416">O `isTaskScheduledAtPriorityOrHigher` método fornece um meio para o código JavaScript determinar se há trabalho pendente nos vários níveis de prioridade \ (ou acima de \) com o intuito de que o código JavaScript de chamada possa decidir gerar um trabalho de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="b0da0-416">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-417">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-417">Example</span></span>**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-418">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="b0da0-418">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-419">Usado para evitar uma atualização do caminho inicial (recarregamento de página) antes de cada evento de ativação \ (por exemplo, clicar em uma notificação ou em um bloco fixado \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-419">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-420">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-420">Parameters</span></span>**  
      
      | <span data-ttu-id="b0da0-421">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-421">Type</span></span> | <span data-ttu-id="b0da0-422">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-422">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-423">Booliano</span><span class="sxs-lookup"><span data-stu-id="b0da0-423">Boolean</span></span> | <span data-ttu-id="b0da0-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` para sempre ignorar a atualização do caminho de início (recarregar página) e, em vez disso, saltar diretamente para acionar o `WebUIApplication` evento ativado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="b0da0-425">Requer que todas as páginas manipulem eventos de ativação separadamente.</span><span class="sxs-lookup"><span data-stu-id="b0da0-425">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="b0da0-426">Ao definir esse método como `true` , clicar em um evento ativado \ (como uma notificação \) não disparará o recarregamento, um essencial para aplicativos de uma única página que desejam evitar recarregamentos de página.</span><span class="sxs-lookup"><span data-stu-id="b0da0-426">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-427">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-427">Return value</span></span>**
      
      <span data-ttu-id="b0da0-428">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-428">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-429">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-429">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-430">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-430">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-431">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-431">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-432">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-432">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-433">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-433">Example</span></span>**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-434">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="b0da0-434">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-435">Controla se um aplicativo suprime possíveis prompts de autenticação durante o download de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0da0-435">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-436">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-436">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="b0da0-437">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-437">[in]</span></span>
      
      | <span data-ttu-id="b0da0-438">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-438">Type</span></span> | <span data-ttu-id="b0da0-439">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-439">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-440">Booliano</span><span class="sxs-lookup"><span data-stu-id="b0da0-440">Boolean</span></span> | <span data-ttu-id="b0da0-441">Um valor de true suprime os prompts de autenticação potencial.</span><span class="sxs-lookup"><span data-stu-id="b0da0-441">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="b0da0-442">Um valor false não elimina qualquer prompt de autenticação potencial do usuário.</span><span class="sxs-lookup"><span data-stu-id="b0da0-442">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-443">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-443">Return value</span></span>**  
      
      <span data-ttu-id="b0da0-444">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-444">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-445">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-445">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-446">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-446">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-447">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-447">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-448">O `suppressSubdownloadCredentialPrompts` método controla se um aplicativo suprime solicitações de autenticação potenciais durante o download de recursos.</span><span class="sxs-lookup"><span data-stu-id="b0da0-448">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="b0da0-449">O comportamento padrão é não suprimir avisos de credenciais.</span><span class="sxs-lookup"><span data-stu-id="b0da0-449">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="b0da0-450">destina-se ao uso por aplicativos que podem carregar um número excessivo de recursos que exigem autenticação, como um aplicativo de email \ (que pode conter um boletim informativo contendo várias imagens em que cada imagem requer autenticação \).</span><span class="sxs-lookup"><span data-stu-id="b0da0-450">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="b0da0-451">Ao suprimir avisos de credenciais, as caixas de diálogo para autenticação em servidores não serão mostradas ao acessar recursos que exigem autenticação, e o recurso não será baixado.</span><span class="sxs-lookup"><span data-stu-id="b0da0-451">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="b0da0-452">Observe que `suppressSubdownloadCredentialPrompts` não afeta outros prompts possíveis, como autenticação de proxy ou solicitação de certificação de cliente, nem afeta o XHR.</span><span class="sxs-lookup"><span data-stu-id="b0da0-452">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="b0da0-453">Lembre-se de que `suppressSubdownloadCredentialPrompts` impacta todo o conteúdo do aplicativo, incluindo o conteúdo hospedado no `webview` elemento.</span><span class="sxs-lookup"><span data-stu-id="b0da0-453">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="b0da0-454">As decisões do prompt de credenciais são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="b0da0-454">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="b0da0-455">Portanto, ao suprimir as solicitações de credenciais entrarão em vigor imediatamente, permitir solicitações de credenciais após supressão delas poderá precisar de um recarregamento do documento para entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="b0da0-455">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-456">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-456">Example</span></span>**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-457">terminateApp</span><span class="sxs-lookup"><span data-stu-id="b0da0-457">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-458">Termina o aplicativo atual e gera um relatório de falhas.</span><span class="sxs-lookup"><span data-stu-id="b0da0-458">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-459">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-459">Parameters</span></span>**  
      
      `error` <span data-ttu-id="b0da0-460">no</span><span class="sxs-lookup"><span data-stu-id="b0da0-460">[in]</span></span>
      
      | <span data-ttu-id="b0da0-461">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-461">Type</span></span> | <span data-ttu-id="b0da0-462">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-462">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-463">Erro</span><span class="sxs-lookup"><span data-stu-id="b0da0-463">Error</span></span> | <span data-ttu-id="b0da0-464">Um `Error` objeto que você pode usar para descrever o erro que disparou o cancelamento.</span><span class="sxs-lookup"><span data-stu-id="b0da0-464">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="b0da0-465">O `Error` objeto deve conter as propriedades Number, Description e Stack; um relatório de falha não será gerado se o objeto não contiver essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0da0-465">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-466">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-466">Return value</span></span>**
      
      <span data-ttu-id="b0da0-467">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-467">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-468">Exceções</span><span class="sxs-lookup"><span data-stu-id="b0da0-468">Exceptions</span></span>**  
      
      <span data-ttu-id="b0da0-469">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-469">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-470">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0da0-470">Remarks</span></span>**  
      
      <span data-ttu-id="b0da0-471">Se o problema relatado `terminateApp` se tornar um dos cinco principais problemas do seu aplicativo, ele será exibido na página de qualidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b0da0-471">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-472">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-472">Example</span></span>**  
      
      <span data-ttu-id="b0da0-473">Este exemplo chama `terminateApp` quando uma exceção é encontrada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-473">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="b0da0-474">Ele usa o `Error` objeto fornecido quando você captura uma exceção.</span><span class="sxs-lookup"><span data-stu-id="b0da0-474">It uses the `Error` object provided when you catch an exception.</span></span>  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b0da0-475">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="b0da0-475">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-476">Valores de prioridade permitidos associados a `execAsyncAtPriority` , `execAtPriority` , `getCurrentPriority` e `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-476">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="b0da0-477">Atual</span><span class="sxs-lookup"><span data-stu-id="b0da0-477">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="b0da0-478">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-478">Type</span></span> | <span data-ttu-id="b0da0-479">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-479">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-480">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-480">DOMString</span></span> | <span data-ttu-id="b0da0-481">Quando `current` usado com o método apropriado \ (consulte também a seção \), o método usará a prioridade contextual atual ao executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-481">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="b0da0-482">Alto</span><span class="sxs-lookup"><span data-stu-id="b0da0-482">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="b0da0-483">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-483">Type</span></span> | <span data-ttu-id="b0da0-484">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-484">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-485">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-485">DOMString</span></span> | <span data-ttu-id="b0da0-486">Quando `high` usado com o método apropriado \ (consulte também a seção \), o método usará maior prioridade normal ao executar a operação solicitada e enviará a operação antes de qualquer trabalho de prioridade normal existente.</span><span class="sxs-lookup"><span data-stu-id="b0da0-486">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="b0da0-487">Ocioso</span><span class="sxs-lookup"><span data-stu-id="b0da0-487">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="b0da0-488">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-488">Type</span></span> | <span data-ttu-id="b0da0-489">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-489">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-490">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-490">DOMString</span></span> | <span data-ttu-id="b0da0-491">Quando `ideal` usado com o método apropriado \ (consulte também a seção \), o método usará a prioridade mais baixa do que o normal ao executar a operação solicitada e enviará a operação após qualquer trabalho normal de prioridade existente.</span><span class="sxs-lookup"><span data-stu-id="b0da0-491">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="b0da0-492">Normal</span><span class="sxs-lookup"><span data-stu-id="b0da0-492">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="b0da0-493">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-493">Type</span></span> | <span data-ttu-id="b0da0-494">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-494">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-495">DOMString</span><span class="sxs-lookup"><span data-stu-id="b0da0-495">DOMString</span></span> | <span data-ttu-id="b0da0-496">Quando `normal` usado com o método apropriado (consulte também a seção), o método usará a prioridade existente normal ao executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="b0da0-496">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-497">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0da0-497">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-498">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0da0-498">Requirements</span></span>**  
      
      | <span data-ttu-id="b0da0-499">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-499">Type</span></span> | <span data-ttu-id="b0da0-500">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-500">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-501">IDL</span><span class="sxs-lookup"><span data-stu-id="b0da0-501">IDL</span></span> | <span data-ttu-id="b0da0-502">Mshtml. idl</span><span class="sxs-lookup"><span data-stu-id="b0da0-502">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="b0da0-503">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="b0da0-503">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <span data-ttu-id="b0da0-504">start</span><span class="sxs-lookup"><span data-stu-id="b0da0-504">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b0da0-505">Inicia o `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-505">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b0da0-506">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0da0-506">Parameters</span></span>**  
      
      <span data-ttu-id="b0da0-507">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-507">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b0da0-508">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b0da0-508">Return value</span></span>**
      
      <span data-ttu-id="b0da0-509">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="b0da0-509">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="b0da0-510">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0da0-510">Properties</span></span>**  
      
      `error` <span data-ttu-id="b0da0-511">folha</span><span class="sxs-lookup"><span data-stu-id="b0da0-511">property</span></span>  
      
      | <span data-ttu-id="b0da0-512">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-512">Type</span></span> | <span data-ttu-id="b0da0-513">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-513">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-514">DOMError</span><span class="sxs-lookup"><span data-stu-id="b0da0-514">DOMError</span></span> | <span data-ttu-id="b0da0-515">Representa um erro em `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-515">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="b0da0-516">folha</span><span class="sxs-lookup"><span data-stu-id="b0da0-516">property</span></span>  
      
      | <span data-ttu-id="b0da0-517">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-517">Type</span></span> | <span data-ttu-id="b0da0-518">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-518">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-519">EventHandler</span><span class="sxs-lookup"><span data-stu-id="b0da0-519">EventHandler</span></span> | <span data-ttu-id="b0da0-520">Propriedade para definir um manipulador de eventos na conclusão de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-520">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="b0da0-521">folha</span><span class="sxs-lookup"><span data-stu-id="b0da0-521">property</span></span>  
      
      | <span data-ttu-id="b0da0-522">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-522">Type</span></span> | <span data-ttu-id="b0da0-523">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-523">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-524">EventHandler</span><span class="sxs-lookup"><span data-stu-id="b0da0-524">EventHandler</span></span> | <span data-ttu-id="b0da0-525">Propriedade para definir um manipulador de eventos em um erro durante `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-525">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="b0da0-526">folha</span><span class="sxs-lookup"><span data-stu-id="b0da0-526">property</span></span>  
      
      | <span data-ttu-id="b0da0-527">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-527">Type</span></span> | <span data-ttu-id="b0da0-528">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-528">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-529">Número</span><span class="sxs-lookup"><span data-stu-id="b0da0-529">Number</span></span> | <span data-ttu-id="b0da0-530">Representa o estado da operação assíncrona dentro do aplicativo do Windows usando JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b0da0-530">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="b0da0-531">Os valores incluem: `Started[0]` , `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-531">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="b0da0-532">folha</span><span class="sxs-lookup"><span data-stu-id="b0da0-532">property</span></span>  
      
      | <span data-ttu-id="b0da0-533">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0da0-533">Type</span></span> | <span data-ttu-id="b0da0-534">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0da0-534">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b0da0-535">Qualquer</span><span class="sxs-lookup"><span data-stu-id="b0da0-535">Any</span></span> |<span data-ttu-id="b0da0-536">Representa o resultado de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="b0da0-536">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
