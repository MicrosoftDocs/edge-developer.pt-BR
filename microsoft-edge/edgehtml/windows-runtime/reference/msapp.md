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
# <a name="msapp"></a>MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

O objeto MSApp e seus membros têm suporte apenas para aplicativos Windows usando JavaScript \(incluindo PWAs acessando recursos da API do Windows\).  O objeto MSApp só existe no contexto local de um documento HTML em um aplicativo do Windows carregado por meio do esquema de URI ms-appx; caso contrário, o objeto não existe (e, consequentemente, nenhum de seus métodos e propriedades estão disponíveis).  

Ele fornece funções auxiliares que permitem criar objetos [Blob](https://developer.mozilla.org/docs/Web/API/Blob) e [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Métodos](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivationActivation](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Constantes](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [current](#current), [high,](#high) [idle](#idle), [normal](#normal).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Interface MSAppAsyncOperation](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [start](#start)  
   :::column-end:::
:::row-end:::  

## <a name="msapp-methods"></a>Métodos MSApp  

### <a name="cleartemporarywebdataasync"></a>clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Limpa os dados de cache e indexadoDB para o aplicativo ou [WebView](../../hosting/webview/index.md).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      Este método não tem parâmetros.  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      Tipo: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
      Representa uma ação assíncrona.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a>createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Cria um [Blob](https://developer.mozilla.org/docs/Web/API/Blob) de um [objeto IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)  Esse método deve ser usado ao lidar com objetos em aplicativos para criar um `IRandomAccessStream` objeto baseado em W3C a partir do fluxo.  Depois que o blob é criado, ele pode ser usado com [o FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [APIs de URL](https://developer.mozilla.org/docs/Web/API/URL)e [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `type` [in]  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | String | Tipo de conteúdo dos dados.  Essa cadeia de caracteres deve estar no formato especificado no token de tipo de mídia definido na seção 3.7 da RFC 2616.  |  
      
      `stream` [in]  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) a ser armazenado no Blob.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Blob | Novo objeto blob que contém o fluxo.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      | Exceção | Condição |  
      |:---- |:--- |  
      | TypeMismatchError | O tipo de nó é incompatível com o tipo de parâmetro esperado.  Para versões anteriores ao Internet Explorer 10, TYPE_MISMATCH_ERR é retornado.  |  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Cria um Blob de tipos do Windows Runtime por meio do namespace MSApp no objeto window.  Este método criará um blob que é essencialmente um invólucro de luz sobre o [objeto RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) fornecido a ele.  O blob é proprietário do tempo de vida desse fluxo e o fluxo será fechado quando o blob for destruído.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
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

### <a name="createdatapackage"></a>createDataPackage  

:::row:::
   :::column span="":::
      Converte o intervalo especificado do usuário ou do aplicativo em um fragmento HTML que pode ser compartilhado.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `object` [in]  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | Esse intervalo pode ser criado a partir de um objeto selection, por exemplo: `window.selection.getRangeAt(0)` , ou manualmente.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | Contém a marcação HTML do intervalo especificado.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Este método dá suporte apenas ao Intervalo dom do modelo de objeto [de documento,](https://developer.mozilla.org/docs/Web/API/Range)não [a TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)  O pacote de dados retornado para o intervalo especificado contém marcação HTML no formato de área de transferência.  
      
      Não há propriedades disponíveis para o pacote de dados retornado.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a>createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Converte a seleção do usuário ou do aplicativo em um fragmento HTML que pode ser compartilhado.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      Este método não tem parâmetros.  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | Contém a marcação HTML do intervalo especificado.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      O pacote de dados retornado para a seleção contém marcação HTML no formato de área de transferência.  Se não houver nenhuma seleção de usuário em qualquer lugar na interface do usuário do aplicativo, o `createDataPackageFromSelection` retornará `null` .  
      
      Não há propriedades disponíveis para o pacote de dados retornado.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a>createFileFromStorageFile  

:::row:::
   :::column span="":::
      Converte um [Arquivo de Armazenamento WinRT](/uwp/api/) [](/uwp/api/windows.storage.storagefile) em um objeto W3C [File](https://developer.mozilla.org/docs/Web/API/File) padrão.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `storageFile` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | Contém o arquivo de armazenamento.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**
      
      Nenhum    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      | Exceção | Condição |  
      |:---- |:--- |  
      | TypeMismatchError | A referência de arquivo W3C especificada é inválida.  Para versões anteriores ao Internet Explorer 10, `TYPE_MISMATCH_ERR` é retornado.  |  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a>createStreamFromInputStream  

:::row:::
   :::column span="":::
      Cria um [MSStream](https://msdn.microsoft.com/library/hh772328) de um [InputStream](https://msdn.microsoft.com/library/hh772327).  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `type` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | Tipo de conteúdo dos dados.  Essa cadeia de caracteres deve estar no formato especificado no token de tipo de mídia definido na seção 3.7 da RFC 2616.  \([Consulte tipos MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) como , , , , , , , `text/plain` , , e assim `text/html` por `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` diante\).  
      
      `inputStream` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | O [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) a ser armazenado no `MSStream` .  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Esse método tem um tipo de conteúdo e a `IInputStream` referência.  Em seguida, o método verifica se a referência de fluxo passada é uma instância do tipo `IInputStream` e, se não for, lança `DOMException TYPE_MISMATCH_ERR` .  Se nenhum erro ocorrer, `createStreamFromInputStream` criará `MSStream` um \(a partir de suas entradas\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      Um `IInputStream` pode ser usado para criar um `MSStream` .  Como são inerentemente objetos de uso único, todas as URLs criadas por são revogadas na primeira vez que são resolvidas `MSStreams` `URL.createObjectURL` pelo elemento image.  Além disso, as solicitações de uma segunda URL nesse objeto após o fluxo ter sido usado falharão.  
      
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

### <a name="execasyncatpriority"></a>execAsyncAtPriority  

:::row:::
   :::column span="":::
      Agenda um retorno de chamada a ser executado posteriormente de acordo com a prioridade determinada.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `asynchronousCallback` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Função | A função de retorno de chamada a ser executado de forma assíncrona, expedida na prioridade determinada.  |  
      
      `priority` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | O valor de prioridade contextual no qual o retorno de chamada assíncronoCallback é executado.  Consulte [Constantes MSApp](#msapp-constants).  |  
      
      `args` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |   
      | Qualquer | Uma série opcional de argumentos que são passados para a função de retorno de chamada síncronaCallback \(como parâmetros 1 e assim por diante\).  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      Este método não retorna um valor.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      A função `asynchronousCallback` de retorno de chamada fornecida é executada de forma assíncrona mais tarde.  `asynchronousCallback` será enviada de acordo com a prioridade fornecida.  A prioridade normal é equivalente ao método [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existente.  Quando o retorno de chamada é executado, a prioridade contextual atual é definida como o valor do parâmetro de prioridade fornecido para a duração da execução do retorno de chamada.  
      
      O `asynchronousCallback` parâmetro callback pode ser qualquer função.  Se os argumentos são fornecidos após `priority` o parâmetro, todos eles serão passados para a função de retorno de chamada.  
      
      Ao contrário de , qualquer objeto retornado pela função de retorno de chamada é `execAtPriority` `asynchronousCallback` ignorado \(e não retornado por `execAsyncAtPriority` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a>execAtPriority  

:::row:::
   :::column span="":::
      Executa a função de retorno de chamada especificada na prioridade contextual determinada.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `synchronousCallback` [in]  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Função | A função de retorno de chamada a ser executado de forma síncrona na prioridade contextual de prioridade determinada.  |  
      
      `priority` [in]  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | O valor de prioridade especificado para o qual o valor de prioridade contextual atual será definido ao executar a `synchronousCallback` função de retorno de chamada.  Consulte [Constantes MSApp](#msapp-constants).  |  
      
      `args` [in]  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | Uma série opcional de argumentos que são passados para a função de retorno de `synchronousCallback` chamada \(como parâmetros 1 e assim por diante\).  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer | Retorna o valor de retorno do `synchronousCallback` retorno de chamada \(conforme aplicável\).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      O método `synchronousCallback` de retorno de chamada fornecido é executado de forma síncrona.  A prioridade contextual atual é alterada para o valor de prioridade fornecido (fornecido pelo argumento priority) durante a duração da função de retorno de chamada fornecida.  Depois que a função de retorno de chamada terminar de executar, a prioridade será retornada para o valor anterior antes da `execAtPriority` chamada.  O valor de `execAtPriority` retorno de é o valor de retorno do método de retorno de chamada \(conforme fornecido\).  
      
      O `synchronousCallback` parâmetro callback pode ser qualquer função.  Se algum argumento for fornecido após o parâmetro priority, eles serão passados para o método de retorno de chamada fornecido.  Se o parâmetro callback retornar um valor, esse valor também se tornará o valor de `execAtPriority` retorno.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
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

### <a name="getcurrentpriority"></a>getCurrentPriority  

:::row:::
   :::column span="":::
      Retorna a prioridade contextual atual.  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | O valor de retorno é uma das cadeias `MSApp.HIGH` de caracteres `MSApp.NORMAL` , ou `MSApp.IDLE` .  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Este método retorna a prioridade contextual atual \(consulte [Constantes MSApp](#msapp-constants)\), que pode ser alterada por `execAtPriority` meio de e `execAsyncAtPriority` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
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

### <a name="gethtmlprintdocumentsource"></a>getHtmlPrintDocumentSource  

API síncrona que foi preterida.  Para o Windows 10, consulte `getHtmlPrintDocumentSourceAsync` .  Para aplicativos windows 8 e 8.1, consulte a entrada MSDN para [obterHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### <a name="gethtmlprintdocumentsourceasync"></a>getHtmlPrintDocumentSourceAsync  

:::row:::
   :::column span="":::
      Retorna o conteúdo de origem que deve ser impresso.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `htmlDoc` [in]  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Documento | O documento HTML a ser impresso.  Pode ser o documento raiz, o documento em um iframe, um fragmento de documento ou um documento SVG.  Esteja ciente de que htmlDoc deve ser um documento, não um elemento.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo 1**  
      
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
      **Exemplo 2**  
      
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

### <a name="getviewid"></a>getViewId  

:::row:::
   :::column span="":::
      Suporte para várias janelas.  
      
      > [!NOTE] 
      > Em Aplicativos UWP JavaScript do Win8.1 suportam várias janelas usando APIs DOM do MSApp que agora estão preteridas.  Para o Windows 10, use `window.open` , e o novo `window` `MSApp.getViewId` .  
      
      | Descrição |Windows 10 | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Criar nova janela | [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Novo objeto window | [janela](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `window`
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | Um objeto que representa uma janela que contém um documento DOM.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      `viewId`
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Número | Pode ser usado com as várias APIs [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) e [window para](https://developer.mozilla.org/docs/Web/API/Window) criar novas janelas, mas para interagir com APIs do WinRT, adicione a `MSApp.getViewId` API.  Ele pega um objeto como parâmetro e retorna um número que pode ser usado com as várias `window` `viewId` APIs [Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  
      
      *   Atrasando a visibilidade  
          
          Os exibições no WinRT normalmente começam ocultos e o desenvolvedor final usa algo como exibir o `TryShowAsStandaloneAsync` exibição quando estiver totalmente preparado.  No mundo da Web, mostra uma janela imediatamente e o usuário final pode assistir à medida que `window.open` o conteúdo é carregado e renderizado.  Para que suas novas janelas agem como exibições no WinRT e não são exibidas imediatamente, adicionamos uma `window.open` opção.  Por exemplo:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Principais diferenças de janela  
          
          A janela primária que é inicialmente aberta pelo sistema operacional age de forma diferente das janelas secundárias que ela abre:  
          
          | Descrição | Primário | Secundária |  
          |:---- |:--- |:--- |  
          | window.open | Permitido | Não permitido |  
          | window.close | Fechar aplicativo | Janela Fechar |  
          | Restrições de navegação | Somente ACUR | Sem restrições |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   Restrições de comunicação de mesma origem  
          
          Há um problema técnico difícil impedindo o suporte adequado para chamadas de script síncronas, de mesma origem, entre janelas.  Quando você abre uma janela que tem a mesma origem, o script em uma janela tem permissão para chamar diretamente funções na outra janela, e algumas dessas chamadas falharão.  `postMessage` chamadas funcionam muito bem e é a maneira recomendada de fazer as coisas, se possível.  O trabalho para melhorar esse problema está em andamento.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a>isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Retorna um valor Boolean indicando se há trabalho pendente no nível de prioridade determinado ou superior.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `priority` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | Um valor de prioridade \(consulte [Constantes do MSApp](#msapp-constants)\) especificando o nível de prioridade e acima para consultar qualquer trabalho em fila pendente.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Booliano | Retorna se houver algum trabalho em fila no `true` nível de prioridade especificado ou acima, caso `false` contrário.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      O método fornece um meio para o código JavaScript determinar se há trabalho pendente nos vários níveis de prioridade \(ou acima\) com a intenção de que o código JavaScript de chamada possa, em seguida, decidir produzir para o trabalho de prioridade `isTaskScheduledAtPriorityOrHigher` mais alta.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
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

### <a name="pagehandlesallapplicationactivations"></a>pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Usado para evitar uma atualização do caminho de início (recarregamento de página) antes de cada evento de ativação \(como clicar em uma notificação ou em um tile fixado\).  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Booliano | Use para sempre ignorar a atualização do caminho de início (recarregamento de página) e, em vez disso, `MSApp.pageHandlesAllApplicationActivations(true)` ir direto para disparar o evento `WebUIApplication` ativado.  Exige que todas as páginas lidam com eventos de ativação separadamente.  Ao definir esse método como , clicar em um evento ativado \(como uma notificação\) não disparará a recarga, um essencial para aplicativos de página única que desejam evitar `true` recarregamentos de página.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
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

### <a name="suppresssubdownloadcredentialprompts"></a>suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Controla se um aplicativo suprime possíveis prompts de autenticação durante o download de recursos.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
     
      `suppress` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Booliano | Um valor verdadeiro suprime possíveis prompts de autenticação.  Um valor false não suprime os prompts de autenticação potenciais do usuário.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**  
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      O `suppressSubdownloadCredentialPrompts` método controla se um aplicativo suprime possíveis prompts de autenticação durante o download de recursos.  O comportamento padrão é não suprimir prompts de credenciais.  
      
      `suppressSubdownloadCredentialPrompts` destina-se a ser usado por aplicativos que podem carregar um número excessivo de recursos que exigem autenticação, como um aplicativo de email \(que poderia conter um boletim informativo contendo várias imagens em que cada imagem requer autenticação\).  
      
      Ao suprimir prompts de credencial, as caixas de diálogo para autenticação em servidores não serão mostradas ao acessar recursos que exigem autenticação e o recurso não será baixado.  Observe que não afeta outros prompts possíveis, como caixas de diálogo de autenticação de proxy ou solicitação de certificação de cliente, nem afeta `suppressSubdownloadCredentialPrompts` xHR.  
      
      Esteja ciente de `suppressSubdownloadCredentialPrompts` que afeta todo o conteúdo do aplicativo, incluindo o conteúdo hospedado no `webview` elemento.  
      
      > [!IMPORTANT]
      > As decisões do prompt de credencial são armazenadas em cache.  Portanto, ao suprimir prompts de credencial terá efeito imediatamente, permitir que os prompts de credencial após suprimi-los possam precisar de uma recarga do documento para fazer efeito.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
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

### <a name="terminateapp"></a>terminateApp  


:::row:::
   :::column span="":::
      Encerra o aplicativo atual e gera um relatório de falha.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      `error` [in]
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Erro | Um `Error` objeto que você pode usar para descrever o erro que disparou a terminação.  O objeto deve conter as propriedades número, descrição e pilha; um relatório de falha não será gerado se o objeto não `Error` conter essas propriedades.  |  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exceções**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Comentários**  
      
      Se o problema relatado por se tornar um dos 5 principais problemas do aplicativo, ele será aparecer na `terminateApp` página Qualidade do aplicativo.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Exemplo**  
      
      Este exemplo chama `terminateApp` quando uma exceção é encontrada.  Ele usa o `Error` objeto fornecido quando você captura uma exceção.  
      
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

### <a name="msapp-constants"></a>Constantes MSApp  

:::row:::
   :::column span="":::
      Valores de prioridade permitidos associados `execAsyncAtPriority` `execAtPriority` a , e `getCurrentPriority` `isTaskScheduldAtPriorityOrHigher` .  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a>Atual  
      
      `current`  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | Quando é usado com o método apropriado \(Consulte também seção\), o método usará a prioridade contextual atual ao `current` executar a operação solicitada.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a>Alto  
      
      `high`  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | Quando é usado com o método apropriado \(Consulte também seção\), o método usará prioridade maior do que a normal ao executar a operação solicitada e será enviado a operação antes de qualquer trabalho de prioridade `high` normal existente.  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a>Ocioso  
      
      `idle`  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | Quando é usado com o método apropriado \(Consulte também seção\), o método usará prioridade inferior à normal ao executar a operação solicitada e será enviado a operação após qualquer trabalho de prioridade `ideal` normal existente.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a>Normal  
      
      `normal`  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMString | Quando é usado com o método apropriado (Consulte também seção), o método usará a prioridade existente normal ao `normal` executar a operação solicitada.  |  
   :::column-end:::
   :::column span="":::
      **Exemplo**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Requisitos**  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | IDL | Mshtml.idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a>MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a>start  

:::row:::
   :::column span="":::
      Inicia o `MSAppAsyncOperation` .  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Parâmetros**  
      
      Nenhuma.  
   :::column-end:::
   :::column span="":::
      **Valor de retorno**
      
      Nenhuma.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **Propriedades**  
      
      `error` property  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | DOMError | Representa um erro em `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` property  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | EventHandler | Propriedade para definir um manipulador de eventos na conclusão de `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` property  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | EventHandler | Propriedade para definir um manipulador de eventos em cima de um erro durante `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` property  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Número | Representa o estado da operação assíncrona no aplicativo Windows usando JavaScript.  Os valores `Started[0]` incluem: `Completed[1]` , , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` property  
      
      | Tipo | Descrição |  
      |:---- |:--- |  
      | Qualquer |Representa o resultado de `MSAppAsyncOperation` .  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
