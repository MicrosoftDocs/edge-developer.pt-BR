---
title: Referência da API MSApp
description: Fornece funções auxiliares que permitem criar objetos Blob e MSStream.  Os objetos e membros do MSApp têm suporte para aplicativos windows usando JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carregamento de arquivo, Blog, MSStream, aplicativos do windows 10, uwp, borda
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0607929971b1dd2956571304230f69f756497e32
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439721"
---
# <a name="msapp"></a><span data-ttu-id="ed188-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="ed188-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="ed188-106">O objeto MSApp e seus membros têm suporte apenas para aplicativos Windows usando JavaScript \(incluindo PWAs acessando recursos da API do Windows\).</span><span class="sxs-lookup"><span data-stu-id="ed188-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="ed188-107">O objeto MSApp só existe no contexto local de um documento HTML em um aplicativo do Windows carregado por meio do esquema de URI ms-appx; caso contrário, o objeto não existe (e, consequentemente, nenhum de seus métodos e propriedades estão disponíveis).</span><span class="sxs-lookup"><span data-stu-id="ed188-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="ed188-108">Ele fornece funções auxiliares que permitem criar objetos [Blob](https://developer.mozilla.org/docs/Web/API/Blob) e [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="ed188-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="ed188-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ed188-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ed188-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivationActivation](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="ed188-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="ed188-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="ed188-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="ed188-112">[current](#current), [high,](#high) [idle](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="ed188-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="ed188-113">Interface MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="ed188-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="ed188-114">start</span><span class="sxs-lookup"><span data-stu-id="ed188-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <a name="msapp-methods"></a><span data-ttu-id="ed188-115">Métodos MSApp</span><span class="sxs-lookup"><span data-stu-id="ed188-115">MSApp methods</span></span>  

### <a name="cleartemporarywebdataasync"></a><span data-ttu-id="ed188-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="ed188-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-117">Limpa os dados de cache e indexadoDB para o aplicativo ou [WebView](../../hosting/webview/index.md).</span><span class="sxs-lookup"><span data-stu-id="ed188-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-118">Parameters</span></span>**  
      
      <span data-ttu-id="ed188-119">Este método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ed188-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-120">Return value</span></span>**  
      
      <span data-ttu-id="ed188-121">Tipo: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="ed188-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="ed188-122">Representa uma ação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ed188-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-123">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-123">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-124">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-125">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-126">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-127">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a><span data-ttu-id="ed188-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="ed188-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-129">Cria um [Blob](https://developer.mozilla.org/docs/Web/API/Blob) de um [objeto IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)</span><span class="sxs-lookup"><span data-stu-id="ed188-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="ed188-130">Esse método deve ser usado ao lidar com objetos em aplicativos para criar um `IRandomAccessStream` objeto baseado em W3C a partir do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ed188-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="ed188-131">Depois que o blob é criado, ele pode ser usado com [o FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [APIs de URL](https://developer.mozilla.org/docs/Web/API/URL)e [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="ed188-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="ed188-133">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-133">[in]</span></span>  
      
      | <span data-ttu-id="ed188-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-134">Type</span></span> | <span data-ttu-id="ed188-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-136">String</span><span class="sxs-lookup"><span data-stu-id="ed188-136">String</span></span> | <span data-ttu-id="ed188-137">Tipo de conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="ed188-137">Content type of the data.</span></span>  <span data-ttu-id="ed188-138">Essa cadeia de caracteres deve estar no formato especificado no token de tipo de mídia definido na seção 3.7 da RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="ed188-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="ed188-139">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-139">[in]</span></span>  
      
      | <span data-ttu-id="ed188-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-140">Type</span></span> | <span data-ttu-id="ed188-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-142">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-142">Any</span></span> | <span data-ttu-id="ed188-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) a ser armazenado no Blob.</span><span class="sxs-lookup"><span data-stu-id="ed188-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-144">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-144">Return value</span></span>**  
      
      | <span data-ttu-id="ed188-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-145">Type</span></span> | <span data-ttu-id="ed188-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-147">Blob</span><span class="sxs-lookup"><span data-stu-id="ed188-147">Blob</span></span> | <span data-ttu-id="ed188-148">Novo objeto blob que contém o fluxo.</span><span class="sxs-lookup"><span data-stu-id="ed188-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-149">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="ed188-150">Exceção</span><span class="sxs-lookup"><span data-stu-id="ed188-150">Exception</span></span> | <span data-ttu-id="ed188-151">Condição</span><span class="sxs-lookup"><span data-stu-id="ed188-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="ed188-152">TypeMismatchError</span></span> | <span data-ttu-id="ed188-153">O tipo de nó é incompatível com o tipo de parâmetro esperado.</span><span class="sxs-lookup"><span data-stu-id="ed188-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="ed188-154">Para versões anteriores ao Internet Explorer 10, TYPE_MISMATCH_ERR é retornado.</span><span class="sxs-lookup"><span data-stu-id="ed188-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-155">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-156">Cria um Blob de tipos do Windows Runtime por meio do namespace MSApp no objeto window.</span><span class="sxs-lookup"><span data-stu-id="ed188-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="ed188-157">Este método criará um blob que é essencialmente um invólucro de luz sobre o [objeto RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) fornecido a ele.</span><span class="sxs-lookup"><span data-stu-id="ed188-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="ed188-158">O blob é proprietário do tempo de vida desse fluxo e o fluxo será fechado quando o blob for destruído.</span><span class="sxs-lookup"><span data-stu-id="ed188-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-159">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-159">Example</span></span>**  
      
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

### <a name="createdatapackage"></a><span data-ttu-id="ed188-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="ed188-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-161">Converte o intervalo especificado do usuário ou do aplicativo em um fragmento HTML que pode ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ed188-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-162">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="ed188-163">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-163">[in]</span></span>  
      
      | <span data-ttu-id="ed188-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-164">Type</span></span> | <span data-ttu-id="ed188-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-166">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-166">Any</span></span> | <span data-ttu-id="ed188-167">Esse intervalo pode ser criado a partir de um objeto selection, por exemplo: `window.selection.getRangeAt(0)` , ou manualmente.</span><span class="sxs-lookup"><span data-stu-id="ed188-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-168">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-168">Return value</span></span>**  
      
      | <span data-ttu-id="ed188-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-169">Type</span></span> | <span data-ttu-id="ed188-170">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-171">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-171">Any</span></span> | <span data-ttu-id="ed188-172">Contém a marcação HTML do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="ed188-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-173">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-173">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-174">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-175">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-175">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-176">Este método dá suporte apenas ao Intervalo dom do modelo de objeto [de documento,](https://developer.mozilla.org/docs/Web/API/Range)não [a TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)</span><span class="sxs-lookup"><span data-stu-id="ed188-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="ed188-177">O pacote de dados retornado para o intervalo especificado contém marcação HTML no formato de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ed188-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="ed188-178">Não há propriedades disponíveis para o pacote de dados retornado.</span><span class="sxs-lookup"><span data-stu-id="ed188-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-179">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-179">Example</span></span>**  
      
      <span data-ttu-id="ed188-180">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a><span data-ttu-id="ed188-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="ed188-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-182">Converte a seleção do usuário ou do aplicativo em um fragmento HTML que pode ser compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ed188-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-183">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-183">Parameters</span></span>**  
      
      <span data-ttu-id="ed188-184">Este método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ed188-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-185">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-185">Return value</span></span>**  
      
      | <span data-ttu-id="ed188-186">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-186">Type</span></span> | <span data-ttu-id="ed188-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-188">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-188">Any</span></span> | <span data-ttu-id="ed188-189">Contém a marcação HTML do intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="ed188-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-190">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-190">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-191">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-192">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-192">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-193">O pacote de dados retornado para a seleção contém marcação HTML no formato de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="ed188-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="ed188-194">Se não houver nenhuma seleção de usuário em qualquer lugar na interface do usuário do aplicativo, o `createDataPackageFromSelection` retornará `null` .</span><span class="sxs-lookup"><span data-stu-id="ed188-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="ed188-195">Não há propriedades disponíveis para o pacote de dados retornado.</span><span class="sxs-lookup"><span data-stu-id="ed188-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-196">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a><span data-ttu-id="ed188-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="ed188-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-198">Converte um [Arquivo de Armazenamento WinRT](/uwp/api/) [](/uwp/api/windows.storage.storagefile) em um objeto W3C [File](https://developer.mozilla.org/docs/Web/API/File) padrão.</span><span class="sxs-lookup"><span data-stu-id="ed188-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-199">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="ed188-200">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-200">[in]</span></span>
      
      | <span data-ttu-id="ed188-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-201">Type</span></span> | <span data-ttu-id="ed188-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-203">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-203">Any</span></span> | <span data-ttu-id="ed188-204">Contém o arquivo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ed188-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-205">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-205">Return value</span></span>**
      
      <span data-ttu-id="ed188-206">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ed188-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-207">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="ed188-208">Exceção</span><span class="sxs-lookup"><span data-stu-id="ed188-208">Exception</span></span> | <span data-ttu-id="ed188-209">Condição</span><span class="sxs-lookup"><span data-stu-id="ed188-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="ed188-210">TypeMismatchError</span></span> | <span data-ttu-id="ed188-211">A referência de arquivo W3C especificada é inválida.</span><span class="sxs-lookup"><span data-stu-id="ed188-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="ed188-212">Para versões anteriores ao Internet Explorer 10, `TYPE_MISMATCH_ERR` é retornado.</span><span class="sxs-lookup"><span data-stu-id="ed188-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-213">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-213">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-214">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-215">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a><span data-ttu-id="ed188-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="ed188-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-217">Cria um [MSStream](https://msdn.microsoft.com/library/hh772328) de um [InputStream](https://msdn.microsoft.com/library/hh772327).</span><span class="sxs-lookup"><span data-stu-id="ed188-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-218">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="ed188-219">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-219">[in]</span></span>
      
      | <span data-ttu-id="ed188-220">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-220">Type</span></span> | <span data-ttu-id="ed188-221">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-222">DOMString</span></span> | <span data-ttu-id="ed188-223">Tipo de conteúdo dos dados.</span><span class="sxs-lookup"><span data-stu-id="ed188-223">Content type of the data.</span></span>  <span data-ttu-id="ed188-224">Essa cadeia de caracteres deve estar no formato especificado no token de tipo de mídia definido na seção 3.7 da RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="ed188-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="ed188-225">\([Consulte tipos MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) como , , , , , , , `text/plain` , , e assim `text/html` por `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` diante\).</span><span class="sxs-lookup"><span data-stu-id="ed188-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="ed188-226">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-226">[in]</span></span>
      
      | <span data-ttu-id="ed188-227">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-227">Type</span></span> | <span data-ttu-id="ed188-228">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-229">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-229">Any</span></span> | <span data-ttu-id="ed188-230">O [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) a ser armazenado no `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="ed188-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-231">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-231">Return value</span></span>**
      
      <span data-ttu-id="ed188-232">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-233">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-233">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-234">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-235">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-235">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-236">Esse método tem um tipo de conteúdo e a `IInputStream` referência.</span><span class="sxs-lookup"><span data-stu-id="ed188-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="ed188-237">Em seguida, o método verifica se a referência de fluxo passada é uma instância do tipo `IInputStream` e, se não for, lança `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="ed188-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="ed188-238">Se nenhum erro ocorrer, `createStreamFromInputStream` criará `MSStream` um \(a partir de suas entradas\).</span><span class="sxs-lookup"><span data-stu-id="ed188-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-239">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-239">Example</span></span>**  
      
      <span data-ttu-id="ed188-240">Um `IInputStream` pode ser usado para criar um `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="ed188-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="ed188-241">Como são inerentemente objetos de uso único, todas as URLs criadas por são revogadas na primeira vez que são resolvidas `MSStreams` `URL.createObjectURL` pelo elemento image.</span><span class="sxs-lookup"><span data-stu-id="ed188-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="ed188-242">Além disso, as solicitações de uma segunda URL nesse objeto após o fluxo ter sido usado falharão.</span><span class="sxs-lookup"><span data-stu-id="ed188-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
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

### <a name="execasyncatpriority"></a><span data-ttu-id="ed188-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="ed188-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-244">Agenda um retorno de chamada a ser executado posteriormente de acordo com a prioridade determinada.</span><span class="sxs-lookup"><span data-stu-id="ed188-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-245">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="ed188-246">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-246">[in]</span></span>
      
      | <span data-ttu-id="ed188-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-247">Type</span></span> | <span data-ttu-id="ed188-248">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-249">Função</span><span class="sxs-lookup"><span data-stu-id="ed188-249">Function</span></span> | <span data-ttu-id="ed188-250">A função de retorno de chamada a ser executado de forma assíncrona, expedida na prioridade determinada.</span><span class="sxs-lookup"><span data-stu-id="ed188-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="ed188-251">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-251">[in]</span></span>
      
      | <span data-ttu-id="ed188-252">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-252">Type</span></span> | <span data-ttu-id="ed188-253">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-254">DOMString</span></span> | <span data-ttu-id="ed188-255">O valor de prioridade contextual no qual o retorno de chamada assíncronoCallback é executado.</span><span class="sxs-lookup"><span data-stu-id="ed188-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="ed188-256">Consulte [Constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="ed188-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="ed188-257">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-257">[in]</span></span>
      
      | <span data-ttu-id="ed188-258">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-258">Type</span></span> | <span data-ttu-id="ed188-259">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="ed188-260">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-260">Any</span></span> | <span data-ttu-id="ed188-261">Uma série opcional de argumentos que são passados para a função de retorno de chamada síncronaCallback \(como parâmetros 1 e assim por diante\).</span><span class="sxs-lookup"><span data-stu-id="ed188-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-262">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-262">Return value</span></span>**  
      
      <span data-ttu-id="ed188-263">Este método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ed188-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-264">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-264">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-265">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-266">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-266">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-267">A função `asynchronousCallback` de retorno de chamada fornecida é executada de forma assíncrona mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ed188-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="ed188-268">será enviada de acordo com a prioridade fornecida.</span><span class="sxs-lookup"><span data-stu-id="ed188-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="ed188-269">A prioridade normal é equivalente ao método [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existente.</span><span class="sxs-lookup"><span data-stu-id="ed188-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="ed188-270">Quando o retorno de chamada é executado, a prioridade contextual atual é definida como o valor do parâmetro de prioridade fornecido para a duração da execução do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ed188-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="ed188-271">O `asynchronousCallback` parâmetro callback pode ser qualquer função.</span><span class="sxs-lookup"><span data-stu-id="ed188-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="ed188-272">Se os argumentos são fornecidos após `priority` o parâmetro, todos eles serão passados para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ed188-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="ed188-273">Ao contrário de , qualquer objeto retornado pela função de retorno de chamada é `execAtPriority` `asynchronousCallback` ignorado \(e não retornado por `execAsyncAtPriority` \).</span><span class="sxs-lookup"><span data-stu-id="ed188-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-274">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a><span data-ttu-id="ed188-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="ed188-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-276">Executa a função de retorno de chamada especificada na prioridade contextual determinada.</span><span class="sxs-lookup"><span data-stu-id="ed188-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-277">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="ed188-278">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-278">[in]</span></span>  
      
      | <span data-ttu-id="ed188-279">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-279">Type</span></span> | <span data-ttu-id="ed188-280">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-281">Função</span><span class="sxs-lookup"><span data-stu-id="ed188-281">Function</span></span> | <span data-ttu-id="ed188-282">A função de retorno de chamada a ser executado de forma síncrona na prioridade contextual de prioridade determinada.</span><span class="sxs-lookup"><span data-stu-id="ed188-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="ed188-283">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-283">[in]</span></span>  
      
      | <span data-ttu-id="ed188-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-284">Type</span></span> | <span data-ttu-id="ed188-285">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-286">DOMString</span></span> | <span data-ttu-id="ed188-287">O valor de prioridade especificado para o qual o valor de prioridade contextual atual será definido ao executar a `synchronousCallback` função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ed188-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="ed188-288">Consulte [Constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="ed188-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="ed188-289">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-289">[in]</span></span>  
      
      | <span data-ttu-id="ed188-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-290">Type</span></span> | <span data-ttu-id="ed188-291">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-292">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-292">Any</span></span> | <span data-ttu-id="ed188-293">Uma série opcional de argumentos que são passados para a função de retorno de `synchronousCallback` chamada \(como parâmetros 1 e assim por diante\).</span><span class="sxs-lookup"><span data-stu-id="ed188-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-294">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-294">Return value</span></span>**  
      
      | <span data-ttu-id="ed188-295">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-295">Type</span></span> | <span data-ttu-id="ed188-296">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-297">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-297">Any</span></span> | <span data-ttu-id="ed188-298">Retorna o valor de retorno do `synchronousCallback` retorno de chamada \(conforme aplicável\).</span><span class="sxs-lookup"><span data-stu-id="ed188-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-299">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-299">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-300">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-301">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-301">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-302">O método `synchronousCallback` de retorno de chamada fornecido é executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="ed188-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="ed188-303">A prioridade contextual atual é alterada para o valor de prioridade fornecido (fornecido pelo argumento priority) durante a duração da função de retorno de chamada fornecida.</span><span class="sxs-lookup"><span data-stu-id="ed188-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="ed188-304">Depois que a função de retorno de chamada terminar de executar, a prioridade será retornada para o valor anterior antes da `execAtPriority` chamada.</span><span class="sxs-lookup"><span data-stu-id="ed188-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="ed188-305">O valor de `execAtPriority` retorno de é o valor de retorno do método de retorno de chamada \(conforme fornecido\).</span><span class="sxs-lookup"><span data-stu-id="ed188-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="ed188-306">O `synchronousCallback` parâmetro callback pode ser qualquer função.</span><span class="sxs-lookup"><span data-stu-id="ed188-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="ed188-307">Se algum argumento for fornecido após o parâmetro priority, eles serão passados para o método de retorno de chamada fornecido.</span><span class="sxs-lookup"><span data-stu-id="ed188-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="ed188-308">Se o parâmetro callback retornar um valor, esse valor também se tornará o valor de `execAtPriority` retorno.</span><span class="sxs-lookup"><span data-stu-id="ed188-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-309">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-309">Example</span></span>**  
      
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

### <a name="getcurrentpriority"></a><span data-ttu-id="ed188-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="ed188-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-311">Retorna a prioridade contextual atual.</span><span class="sxs-lookup"><span data-stu-id="ed188-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-312">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-312">Parameters</span></span>**  
      
      <span data-ttu-id="ed188-313">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-314">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-314">Return value</span></span>**  
      
      | <span data-ttu-id="ed188-315">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-315">Type</span></span> | <span data-ttu-id="ed188-316">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-317">DOMString</span></span> | <span data-ttu-id="ed188-318">O valor de retorno é uma das cadeias `MSApp.HIGH` de caracteres `MSApp.NORMAL` , ou `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="ed188-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-319">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-319">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-320">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-321">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-321">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-322">Este método retorna a prioridade contextual atual \(consulte [Constantes MSApp](#msapp-constants)\), que pode ser alterada por `execAtPriority` meio de e `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="ed188-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-323">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-323">Example</span></span>**  
      
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

### <a name="gethtmlprintdocumentsource"></a><span data-ttu-id="ed188-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="ed188-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="ed188-325">API síncrona que foi preterida.</span><span class="sxs-lookup"><span data-stu-id="ed188-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="ed188-326">Para o Windows 10, consulte `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="ed188-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="ed188-327">Para aplicativos windows 8 e 8.1, consulte a entrada MSDN para [obterHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="ed188-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <a name="gethtmlprintdocumentsourceasync"></a><span data-ttu-id="ed188-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="ed188-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-329">Retorna o conteúdo de origem que deve ser impresso.</span><span class="sxs-lookup"><span data-stu-id="ed188-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-330">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="ed188-331">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-331">[in]</span></span>  
      
      | <span data-ttu-id="ed188-332">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-332">Type</span></span> | <span data-ttu-id="ed188-333">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-334">Documento</span><span class="sxs-lookup"><span data-stu-id="ed188-334">Document</span></span> | <span data-ttu-id="ed188-335">O documento HTML a ser impresso.</span><span class="sxs-lookup"><span data-stu-id="ed188-335">The HTML document to be printed.</span></span>  <span data-ttu-id="ed188-336">Pode ser o documento raiz, o documento em um iframe, um fragmento de documento ou um documento SVG.</span><span class="sxs-lookup"><span data-stu-id="ed188-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="ed188-337">Esteja ciente de que htmlDoc deve ser um documento, não um elemento.</span><span class="sxs-lookup"><span data-stu-id="ed188-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-338">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-338">Return value</span></span>**
      
      <span data-ttu-id="ed188-339">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-340">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-340">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-341">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-342">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-342">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-343">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-344">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed188-344">Example 1</span></span>**  
      
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
      **<span data-ttu-id="ed188-345">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ed188-345">Example 2</span></span>**  
      
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

### <a name="getviewid"></a><span data-ttu-id="ed188-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="ed188-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-347">Suporte para várias janelas.</span><span class="sxs-lookup"><span data-stu-id="ed188-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="ed188-348">Em Aplicativos UWP JavaScript do Win8.1 suportam várias janelas usando APIs DOM do MSApp que agora estão preteridas.</span><span class="sxs-lookup"><span data-stu-id="ed188-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="ed188-349">Para o Windows 10, use `window.open` , e o novo `window` `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="ed188-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="ed188-350">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-350">Description</span></span> |<span data-ttu-id="ed188-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed188-351">Windows 10</span></span> | <span data-ttu-id="ed188-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ed188-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="ed188-353">Criar nova janela</span><span class="sxs-lookup"><span data-stu-id="ed188-353">Create new window</span></span> | [<span data-ttu-id="ed188-354">window.open</span><span class="sxs-lookup"><span data-stu-id="ed188-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="ed188-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="ed188-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="ed188-356">Novo objeto window</span><span class="sxs-lookup"><span data-stu-id="ed188-356">New window object</span></span> | [<span data-ttu-id="ed188-357">janela</span><span class="sxs-lookup"><span data-stu-id="ed188-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="ed188-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="ed188-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-359">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="ed188-360">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-360">Type</span></span> | <span data-ttu-id="ed188-361">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-362">DOMString</span></span> | <span data-ttu-id="ed188-363">Um objeto que representa uma janela que contém um documento DOM.</span><span class="sxs-lookup"><span data-stu-id="ed188-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-364">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="ed188-365">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-365">Type</span></span> | <span data-ttu-id="ed188-366">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-367">Número</span><span class="sxs-lookup"><span data-stu-id="ed188-367">Number</span></span> | <span data-ttu-id="ed188-368">Pode ser usado com as várias APIs [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="ed188-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-369">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-369">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-370">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-371">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-371">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) e [window para](https://developer.mozilla.org/docs/Web/API/Window) criar novas janelas, mas para interagir com APIs do WinRT, adicione a `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="ed188-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="ed188-373">Ele pega um objeto como parâmetro e retorna um número que pode ser usado com as várias `window` `viewId` APIs [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="ed188-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="ed188-374">Atrasando a visibilidade</span><span class="sxs-lookup"><span data-stu-id="ed188-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="ed188-375">Os exibições no WinRT normalmente começam ocultos e o desenvolvedor final usa algo como exibir o `TryShowAsStandaloneAsync` exibição quando estiver totalmente preparado.</span><span class="sxs-lookup"><span data-stu-id="ed188-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="ed188-376">No mundo da Web, mostra uma janela imediatamente e o usuário final pode assistir à medida que `window.open` o conteúdo é carregado e renderizado.</span><span class="sxs-lookup"><span data-stu-id="ed188-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="ed188-377">Para que suas novas janelas agem como exibições no WinRT e não são exibidas imediatamente, adicionamos uma `window.open` opção.</span><span class="sxs-lookup"><span data-stu-id="ed188-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="ed188-378">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ed188-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="ed188-379">Principais diferenças de janela</span><span class="sxs-lookup"><span data-stu-id="ed188-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="ed188-380">A janela primária que é inicialmente aberta pelo sistema operacional age de forma diferente das janelas secundárias que ela abre:</span><span class="sxs-lookup"><span data-stu-id="ed188-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="ed188-381">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-381">Description</span></span> | <span data-ttu-id="ed188-382">Primário</span><span class="sxs-lookup"><span data-stu-id="ed188-382">Primary</span></span> | <span data-ttu-id="ed188-383">Secundária</span><span class="sxs-lookup"><span data-stu-id="ed188-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="ed188-384">window.open</span><span class="sxs-lookup"><span data-stu-id="ed188-384">window.open</span></span> | <span data-ttu-id="ed188-385">Permitido</span><span class="sxs-lookup"><span data-stu-id="ed188-385">Allowed</span></span> | <span data-ttu-id="ed188-386">Não permitido</span><span class="sxs-lookup"><span data-stu-id="ed188-386">Disallowed</span></span> |  
          | <span data-ttu-id="ed188-387">window.close</span><span class="sxs-lookup"><span data-stu-id="ed188-387">window.close</span></span> | <span data-ttu-id="ed188-388">Fechar aplicativo</span><span class="sxs-lookup"><span data-stu-id="ed188-388">Close app</span></span> | <span data-ttu-id="ed188-389">Janela Fechar</span><span class="sxs-lookup"><span data-stu-id="ed188-389">Close window</span></span> |  
          | <span data-ttu-id="ed188-390">Restrições de navegação</span><span class="sxs-lookup"><span data-stu-id="ed188-390">Navigation restrictions</span></span> | <span data-ttu-id="ed188-391">Somente ACUR</span><span class="sxs-lookup"><span data-stu-id="ed188-391">ACUR only</span></span> | <span data-ttu-id="ed188-392">Sem restrições</span><span class="sxs-lookup"><span data-stu-id="ed188-392">No restrictions</span></span> |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   <span data-ttu-id="ed188-393">Restrições de comunicação de mesma origem</span><span class="sxs-lookup"><span data-stu-id="ed188-393">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="ed188-394">Há um problema técnico difícil impedindo o suporte adequado para chamadas de script síncronas, de mesma origem, entre janelas.</span><span class="sxs-lookup"><span data-stu-id="ed188-394">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="ed188-395">Quando você abre uma janela que tem a mesma origem, o script em uma janela tem permissão para chamar diretamente funções na outra janela, e algumas dessas chamadas falharão.</span><span class="sxs-lookup"><span data-stu-id="ed188-395">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="ed188-396">chamadas funcionam muito bem e é a maneira recomendada de fazer as coisas, se possível.</span><span class="sxs-lookup"><span data-stu-id="ed188-396">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="ed188-397">O trabalho para melhorar esse problema está em andamento.</span><span class="sxs-lookup"><span data-stu-id="ed188-397">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-398">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-398">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a><span data-ttu-id="ed188-399">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="ed188-399">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-400">Retorna um valor Boolean indicando se há trabalho pendente no nível de prioridade determinado ou superior.</span><span class="sxs-lookup"><span data-stu-id="ed188-400">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-401">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-401">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="ed188-402">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-402">[in]</span></span>
      
      | <span data-ttu-id="ed188-403">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-403">Type</span></span> | <span data-ttu-id="ed188-404">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-404">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-405">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-405">DOMString</span></span> | <span data-ttu-id="ed188-406">Um valor de prioridade \(consulte [Constantes do MSApp](#msapp-constants)\) especificando o nível de prioridade e acima para consultar qualquer trabalho em fila pendente.</span><span class="sxs-lookup"><span data-stu-id="ed188-406">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-407">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-407">Return value</span></span>**  
      
      | <span data-ttu-id="ed188-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-408">Type</span></span> | <span data-ttu-id="ed188-409">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-409">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-410">Booliano</span><span class="sxs-lookup"><span data-stu-id="ed188-410">Boolean</span></span> | <span data-ttu-id="ed188-411">Retorna se houver algum trabalho em fila no `true` nível de prioridade especificado ou acima, caso `false` contrário.</span><span class="sxs-lookup"><span data-stu-id="ed188-411">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-412">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-412">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-413">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-413">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-414">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-414">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-415">O método fornece um meio para o código JavaScript determinar se há trabalho pendente nos vários níveis de prioridade \(ou acima\) com a intenção de que o código JavaScript de chamada possa, em seguida, decidir produzir para o trabalho de prioridade `isTaskScheduledAtPriorityOrHigher` mais alta.</span><span class="sxs-lookup"><span data-stu-id="ed188-415">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-416">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-416">Example</span></span>**  
      
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

### <a name="pagehandlesallapplicationactivations"></a><span data-ttu-id="ed188-417">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="ed188-417">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-418">Usado para evitar uma atualização do caminho de início (recarregamento de página) antes de cada evento de ativação \(como clicar em uma notificação ou em um tile fixado\).</span><span class="sxs-lookup"><span data-stu-id="ed188-418">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-419">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-419">Parameters</span></span>**  
      
      | <span data-ttu-id="ed188-420">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-420">Type</span></span> | <span data-ttu-id="ed188-421">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-421">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-422">Booliano</span><span class="sxs-lookup"><span data-stu-id="ed188-422">Boolean</span></span> | <span data-ttu-id="ed188-423">Use para sempre ignorar a atualização do caminho de início (recarregamento de página) e, em vez disso, `MSApp.pageHandlesAllApplicationActivations(true)` ir direto para disparar o evento `WebUIApplication` ativado.</span><span class="sxs-lookup"><span data-stu-id="ed188-423">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="ed188-424">Exige que todas as páginas lidam com eventos de ativação separadamente.</span><span class="sxs-lookup"><span data-stu-id="ed188-424">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="ed188-425">Ao definir esse método como , clicar em um evento ativado \(como uma notificação\) não disparará a recarga, um essencial para aplicativos de página única que desejam evitar `true` recarregamentos de página.</span><span class="sxs-lookup"><span data-stu-id="ed188-425">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-426">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-426">Return value</span></span>**
      
      <span data-ttu-id="ed188-427">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-427">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-428">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-428">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-429">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-429">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-430">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-430">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-431">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-431">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-432">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-432">Example</span></span>**  
      
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

### <a name="suppresssubdownloadcredentialprompts"></a><span data-ttu-id="ed188-433">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="ed188-433">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-434">Controla se um aplicativo suprime possíveis prompts de autenticação durante o download de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed188-434">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-435">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-435">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="ed188-436">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-436">[in]</span></span>
      
      | <span data-ttu-id="ed188-437">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-437">Type</span></span> | <span data-ttu-id="ed188-438">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-438">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-439">Booliano</span><span class="sxs-lookup"><span data-stu-id="ed188-439">Boolean</span></span> | <span data-ttu-id="ed188-440">Um valor verdadeiro suprime possíveis prompts de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ed188-440">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="ed188-441">Um valor false não suprime os prompts de autenticação potenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="ed188-441">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-442">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-442">Return value</span></span>**  
      
      <span data-ttu-id="ed188-443">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-443">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-444">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-444">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-445">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-445">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-446">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-446">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-447">O `suppressSubdownloadCredentialPrompts` método controla se um aplicativo suprime possíveis prompts de autenticação durante o download de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed188-447">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="ed188-448">O comportamento padrão é não suprimir prompts de credenciais.</span><span class="sxs-lookup"><span data-stu-id="ed188-448">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="ed188-449">destina-se a ser usado por aplicativos que podem carregar um número excessivo de recursos que exigem autenticação, como um aplicativo de email \(que poderia conter um boletim informativo contendo várias imagens em que cada imagem requer autenticação\).</span><span class="sxs-lookup"><span data-stu-id="ed188-449">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="ed188-450">Ao suprimir prompts de credencial, as caixas de diálogo para autenticação em servidores não serão mostradas ao acessar recursos que exigem autenticação e o recurso não será baixado.</span><span class="sxs-lookup"><span data-stu-id="ed188-450">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="ed188-451">Observe que não afeta outros prompts possíveis, como caixas de diálogo de autenticação de proxy ou solicitação de certificação de cliente, nem afeta `suppressSubdownloadCredentialPrompts` xHR.</span><span class="sxs-lookup"><span data-stu-id="ed188-451">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="ed188-452">Esteja ciente de `suppressSubdownloadCredentialPrompts` que afeta todo o conteúdo do aplicativo, incluindo o conteúdo hospedado no `webview` elemento.</span><span class="sxs-lookup"><span data-stu-id="ed188-452">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="ed188-453">As decisões do prompt de credencial são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="ed188-453">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="ed188-454">Portanto, ao suprimir prompts de credencial terá efeito imediatamente, permitir que os prompts de credencial após suprimi-los possam precisar de uma recarga do documento para fazer efeito.</span><span class="sxs-lookup"><span data-stu-id="ed188-454">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-455">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-455">Example</span></span>**  
      
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

### <a name="terminateapp"></a><span data-ttu-id="ed188-456">terminateApp</span><span class="sxs-lookup"><span data-stu-id="ed188-456">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-457">Encerra o aplicativo atual e gera um relatório de falha.</span><span class="sxs-lookup"><span data-stu-id="ed188-457">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-458">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-458">Parameters</span></span>**  
      
      `error` <span data-ttu-id="ed188-459">[in]</span><span class="sxs-lookup"><span data-stu-id="ed188-459">[in]</span></span>
      
      | <span data-ttu-id="ed188-460">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-460">Type</span></span> | <span data-ttu-id="ed188-461">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-461">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-462">Erro</span><span class="sxs-lookup"><span data-stu-id="ed188-462">Error</span></span> | <span data-ttu-id="ed188-463">Um `Error` objeto que você pode usar para descrever o erro que disparou a terminação.</span><span class="sxs-lookup"><span data-stu-id="ed188-463">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="ed188-464">O objeto deve conter as propriedades número, descrição e pilha; um relatório de falha não será gerado se o objeto não `Error` conter essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ed188-464">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-465">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-465">Return value</span></span>**
      
      <span data-ttu-id="ed188-466">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-466">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-467">Exceções</span><span class="sxs-lookup"><span data-stu-id="ed188-467">Exceptions</span></span>**  
      
      <span data-ttu-id="ed188-468">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-468">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-469">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed188-469">Remarks</span></span>**  
      
      <span data-ttu-id="ed188-470">Se o problema relatado por se tornar um dos 5 principais problemas do aplicativo, ele será aparecer na `terminateApp` página Qualidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed188-470">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-471">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-471">Example</span></span>**  
      
      <span data-ttu-id="ed188-472">Este exemplo chama `terminateApp` quando uma exceção é encontrada.</span><span class="sxs-lookup"><span data-stu-id="ed188-472">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="ed188-473">Ele usa o `Error` objeto fornecido quando você captura uma exceção.</span><span class="sxs-lookup"><span data-stu-id="ed188-473">It uses the `Error` object provided when you catch an exception.</span></span>  
      
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

### <a name="msapp-constants"></a><span data-ttu-id="ed188-474">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="ed188-474">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-475">Valores de prioridade permitidos associados `execAsyncAtPriority` `execAtPriority` a , e `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="ed188-475">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a><span data-ttu-id="ed188-476">Atual</span><span class="sxs-lookup"><span data-stu-id="ed188-476">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="ed188-477">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-477">Type</span></span> | <span data-ttu-id="ed188-478">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-478">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-479">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-479">DOMString</span></span> | <span data-ttu-id="ed188-480">Quando é usado com o método apropriado \(Consulte também seção\), o método usará a prioridade contextual atual ao `current` executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ed188-480">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a><span data-ttu-id="ed188-481">Alto</span><span class="sxs-lookup"><span data-stu-id="ed188-481">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="ed188-482">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-482">Type</span></span> | <span data-ttu-id="ed188-483">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-483">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-484">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-484">DOMString</span></span> | <span data-ttu-id="ed188-485">Quando é usado com o método apropriado \(Consulte também seção\), o método usará prioridade maior do que a normal ao executar a operação solicitada e será enviado a operação antes de qualquer trabalho de prioridade `high` normal existente.</span><span class="sxs-lookup"><span data-stu-id="ed188-485">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a><span data-ttu-id="ed188-486">Ocioso</span><span class="sxs-lookup"><span data-stu-id="ed188-486">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="ed188-487">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-487">Type</span></span> | <span data-ttu-id="ed188-488">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-488">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-489">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-489">DOMString</span></span> | <span data-ttu-id="ed188-490">Quando é usado com o método apropriado \(Consulte também seção\), o método usará prioridade inferior à normal ao executar a operação solicitada e será enviado a operação após qualquer trabalho de prioridade `ideal` normal existente.</span><span class="sxs-lookup"><span data-stu-id="ed188-490">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a><span data-ttu-id="ed188-491">Normal</span><span class="sxs-lookup"><span data-stu-id="ed188-491">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="ed188-492">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-492">Type</span></span> | <span data-ttu-id="ed188-493">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-493">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-494">DOMString</span><span class="sxs-lookup"><span data-stu-id="ed188-494">DOMString</span></span> | <span data-ttu-id="ed188-495">Quando é usado com o método apropriado (Consulte também seção), o método usará a prioridade existente normal ao `normal` executar a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="ed188-495">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-496">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ed188-496">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-497">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed188-497">Requirements</span></span>**  
      
      | <span data-ttu-id="ed188-498">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-498">Type</span></span> | <span data-ttu-id="ed188-499">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-499">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-500">IDL</span><span class="sxs-lookup"><span data-stu-id="ed188-500">IDL</span></span> | <span data-ttu-id="ed188-501">Mshtml.idl</span><span class="sxs-lookup"><span data-stu-id="ed188-501">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a><span data-ttu-id="ed188-502">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="ed188-502">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a><span data-ttu-id="ed188-503">start</span><span class="sxs-lookup"><span data-stu-id="ed188-503">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ed188-504">Inicia o `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="ed188-504">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="ed188-505">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed188-505">Parameters</span></span>**  
      
      <span data-ttu-id="ed188-506">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-506">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="ed188-507">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ed188-507">Return value</span></span>**
      
      <span data-ttu-id="ed188-508">Nenhuma.</span><span class="sxs-lookup"><span data-stu-id="ed188-508">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="ed188-509">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ed188-509">Properties</span></span>**  
      
      `error` <span data-ttu-id="ed188-510">property</span><span class="sxs-lookup"><span data-stu-id="ed188-510">property</span></span>  
      
      | <span data-ttu-id="ed188-511">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-511">Type</span></span> | <span data-ttu-id="ed188-512">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-512">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-513">DOMError</span><span class="sxs-lookup"><span data-stu-id="ed188-513">DOMError</span></span> | <span data-ttu-id="ed188-514">Representa um erro em `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="ed188-514">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="ed188-515">property</span><span class="sxs-lookup"><span data-stu-id="ed188-515">property</span></span>  
      
      | <span data-ttu-id="ed188-516">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-516">Type</span></span> | <span data-ttu-id="ed188-517">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-517">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-518">EventHandler</span><span class="sxs-lookup"><span data-stu-id="ed188-518">EventHandler</span></span> | <span data-ttu-id="ed188-519">Propriedade para definir um manipulador de eventos na conclusão de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="ed188-519">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="ed188-520">property</span><span class="sxs-lookup"><span data-stu-id="ed188-520">property</span></span>  
      
      | <span data-ttu-id="ed188-521">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-521">Type</span></span> | <span data-ttu-id="ed188-522">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-522">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-523">EventHandler</span><span class="sxs-lookup"><span data-stu-id="ed188-523">EventHandler</span></span> | <span data-ttu-id="ed188-524">Propriedade para definir um manipulador de eventos em cima de um erro durante `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="ed188-524">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="ed188-525">property</span><span class="sxs-lookup"><span data-stu-id="ed188-525">property</span></span>  
      
      | <span data-ttu-id="ed188-526">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-526">Type</span></span> | <span data-ttu-id="ed188-527">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-527">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-528">Número</span><span class="sxs-lookup"><span data-stu-id="ed188-528">Number</span></span> | <span data-ttu-id="ed188-529">Representa o estado da operação assíncrona no aplicativo Windows usando JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ed188-529">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="ed188-530">Os valores `Started[0]` incluem: `Completed[1]` , , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="ed188-530">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="ed188-531">property</span><span class="sxs-lookup"><span data-stu-id="ed188-531">property</span></span>  
      
      | <span data-ttu-id="ed188-532">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed188-532">Type</span></span> | <span data-ttu-id="ed188-533">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed188-533">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="ed188-534">Qualquer</span><span class="sxs-lookup"><span data-stu-id="ed188-534">Any</span></span> |<span data-ttu-id="ed188-535">Representa o resultado de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="ed188-535">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
