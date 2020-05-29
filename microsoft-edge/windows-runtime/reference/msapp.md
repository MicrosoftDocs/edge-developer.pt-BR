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
# MSApp

O objeto MSApp e seus membros têm suporte somente para aplicativos do Windows que usam JavaScript (incluindo PWAs acessando recursos da API do Windows). O objeto MSApp existe somente no contexto local de um documento HTML em um aplicativo do Windows carregado por meio do esquema de URI MS-Appx; caso contrário, o objeto não existe (e conseqüentemente, nenhum de seus métodos e propriedades estão disponíveis).

Ele fornece funções auxiliares que permitem criar objetos [blob](https://developer.mozilla.org/docs/Web/API/Blob) e [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**Métodos**](#msapp-methods) | [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getviewid](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp). |

| | |
| :--- | :--- |
| [**:**](#msapp-constants) | [atual](#current), [alto](#high), [ocioso](#idle), [normal](#normal).|

| | |
| :--- | :--- |
| [Interface **MSAppAsyncOperation**](#msappasyncoperation) | [start](#start) |

## Métodos MSApp

### clearTemporaryWebDataAsync 
Limpa o cache e os dados do indexedDB para o aplicativo ou [WebView](../../webview.md).

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### Parâmetros
Esse método não tem parâmetros.

#### Valor de retorno
Digite[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)

Representa uma ação assíncrona.

### createBlobFromRandomAccessStream
Cria um [blob](https://developer.mozilla.org/docs/Web/API/Blob) a partir de um [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) objeto. Esse método deve ser usado ao lidar com `IRandomAccessStream` objetos em aplicativos para criar um objeto baseado no W3C a partir do Stream. Depois que o blob é criado, ele pode ser usado com o [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [APIs de URL](https://developer.mozilla.org/docs/Web/API/URL)e [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest). 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### Parâmetros

`type` no

|Tipo | Descrição |
|:---- |:--- |
|String | Tipo de conteúdo dos dados. Essa cadeia de caracteres deve estar no formato especificado no token do tipo de mídia definido na seção 3,7 da RFC 2616.

`stream` no

|Tipo | Descrição |
|:---- |:--- |
|Qualquer | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) a ser armazenado no BLOB.

#### Valor de retorno
|Tipo | Descrição |
|:---- |:--- |
|Irregular | Novo objeto BLOB que contém o fluxo.

#### Exceções
|Extremamente | Condição |
|:---- |:--- |
|TypeMismatchError | O tipo de nó é incompatível com o tipo de parâmetro esperado. Para versões anteriores ao Internet Explorer 10, TYPE_MISMATCH_ERR é retornado.

#### Comentários
Cria um blob a partir de tipos do Windows Runtime por meio do namespace MSApp no objeto Window. Esse método criará um blob que é essencialmente um wrapper claro sobre o [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) objeto fornecido a ele. O blob é proprietário do tempo de vida desse fluxo e o fluxo será fechado quando o blob for destruído. 

#### Exemplo

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### createDataPackage
Converte o intervalo especificado do usuário ou do aplicativo em um fragmento de HTML que pode ser compartilhado.

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### Parâmetros
`object` no

|Tipo | Descrição |
|:---- |:--- |
|Qualquer | Esse intervalo pode ser criado a partir de um objeto Selection, por exemplo: `window.selection.getRangeAt(0)` ou manualmente.

#### Valor de retorno
|Tipo | Descrição |
|:---- |:--- |
|Qualquer | Contém a marcação HTML para o intervalo especificado.

#### Comentários
Esse método oferece suporte somente ao [intervalo dom](https://developer.mozilla.org/docs/Web/API/Range), e não a [TextRange](/uwp/api/windows.ui.xaml.documents.textrange). O pacote de dados retornado para o intervalo especificado contém marcação HTML no formato da área de transferência.

Não há propriedades disponíveis para o pacote de dados retornado.

### createDataPackageFromSelection 
Converte a seleção do usuário ou do aplicativo em um fragmento HTML que pode ser compartilhado.

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### Parâmetros
Esse método não tem parâmetros.

#### Valor de retorno
|Tipo | Descrição |
|:---- |:--- |
|Qualquer | Contém a marcação HTML para o intervalo especificado.

#### Comentários
O pacote de dados retornado para a seleção contém marcação HTML no formato da área de transferência. Se não houver nenhuma seleção de usuário em qualquer lugar dentro da interface do usuário do aplicativo, o `createDataPackageFromSelection` retorna NULL.

Não há propriedades disponíveis para o pacote de dados retornado.
 
### createFileFromStorageFile 
Converte um [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) em um objeto W3C padrão [`File`](https://developer.mozilla.org/docs/Web/API/File) .

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### Parâmetros
`storageFile` no

|Tipo | Descrição |
|:---- |:--- |
|Qualquer | Contém o arquivo de armazenamento.

#### Exceções
|Extremamente | Condição |
|:---- |:--- |
|TypeMismatchError | A referência do arquivo W3C especificado é inválida. Para versões anteriores ao Internet Explorer 10, TYPE_MISMATCH_ERR é retornado.

### createStreamFromInputStream  

Cria um [`MSStream`](https://msdn.microsoft.com/library/hh772328) de [`InputStream`](https://msdn.microsoft.com/library/hh772327) .  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### Parâmetros
`type` no

|Tipo | Descrição |
|:---- |:--- |
|DOMString | Tipo de conteúdo dos dados. Essa cadeia de caracteres deve estar no formato especificado no token do tipo de mídia definido na seção 3,7 da RFC 2616. ([Veja tipos MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. text/plain, text/html, image/jpeg, image/png, Audio/MPEG, Audio/OGG, Audio/*, Video/MP4, etc.). 

`inputStream` no

|Tipo | Descrição |
|:---- |:--- |
|Qualquer | A [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) a ser armazenada no `MSStream` .

#### Comentários
Esse método assume um tipo de conteúdo e a `IInputStream` referência. Em seguida, o método verifica se a referência do fluxo transmitida é uma instância do tipo `IInputStream` e, se não for, throws `DOMException TYPE_MISMATCH_ERR` . Se não ocorrerem erros, `createStreamFromInputStream` o cria uma `MSStream` (a partir de suas entradas).

#### Exemplo
Um `IInputStream` pode ser usado para criar um `MSStream` . Como `MSStreams` são objetos inerentemente de uso único, todas as URLs criadas por `URL.createObjectURL` são revogadas na primeira vez que são resolvidas pelo elemento Image. Além disso, as solicitações para uma segunda URL neste objeto após o fluxo ter sido usado falharão.

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### execAsyncAtPriority 
Agenda um retorno de chamada para ser executado em um momento posterior, de acordo com a prioridade determinada. 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### Parâmetros
`asynchronousCallback` no

|Tipo | Descrição |
|:---- |:--- |
|Função | A função de retorno de chamada para ser executada de forma assíncrona, despachada com a prioridade determinada.

`priority` no

|Tipo | Descrição |
|:---- |:--- |
|DOMString | O valor de prioridade contextual no qual o retorno de chamada do asynchronousCallback é executado. Consulte [constantes MSApp](#msapp-constants).

`args` no

|Tipo | Descrição |
|:---- |:--- |
|Qualquer | Uma série opcional de argumentos que são passados para a função de retorno de chamada synchronousCallback (como parâmetros 1 e on).

#### Valor de retorno
Esse método não retorna um valor.

#### Comentários
A `asynchronousCallback` função de retorno de chamada fornecida será executada de forma assíncrona mais tarde. `asynchronousCallback` será despachado de acordo com a prioridade fornecida. A prioridade normal equivale ao método existente [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) . Quando o retorno de chamada é executado, a prioridade contextual atual é definida como o valor de parâmetro de prioridade fornecido para a duração da execução do retorno de chamada.

O `asynchronousCallback` parâmetro callback pode ser qualquer função. Se os argumentos forem fornecidos após o `priority` parâmetro, todos serão passados para a função de retorno de chamada.

Ao contrário `execAtPriority` , qualquer objeto retornado pela `asynchronousCallback` função de retorno de chamada é ignorado (e não é retornado via `execAsyncAtPriority` ).

### execAtPriority 
Executa a função de retorno de chamada especificada na prioridade contextual determinada.

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### Parâmetros
`synchronousCallback` no

|Tipo | Descrição |
|:---- |:--- |
|Função | A função de retorno de chamada a ser executada de forma síncrona na prioridade contextual determinada prioridade.

`priority` no

|Tipo | Descrição |
|:---- |:--- |
|DOMString | O valor de prioridade especificado ao qual o valor de prioridade contextual atual será definido ao executar a `synchronousCallback` função de retorno de chamada. Consulte [constantes MSApp](#msapp-constants).

`args` no

|Tipo | Descrição |
|:---- |:--- |
|Qualquer | Uma série opcional de argumentos que são passados para a `synchronousCallback` função de retorno de chamada (como parâmetros 1 e ativado).

#### Valor de retorno
|Tipo | Descrição |
|:---- |:--- |
|Qualquer | Retorna o valor de retorno do `synchronousCallback` retorno de chamada (conforme aplicável).

#### Comentários
O `synchronousCallback` método callback fornecido é executado de forma síncrona. A prioridade contextual atual é alterada para o valor de prioridade fornecido (fornecido pelo argumento Priority) para a duração da função de retorno de chamada fornecida. Depois que a execução da função de retorno de chamada terminar, a prioridade será retornada ao valor anterior antes da `execAtPriority` chamada. O valor de retorno `execAtPriority` é o valor de retorno do método callback (conforme fornecido).
 
O `synchronousCallback` parâmetro callback pode ser qualquer função. Se algum argumento for fornecido após o parâmetro Priority, ele será passado para o método callback fornecido. Se o parâmetro callback retornar um valor, esse valor também se tornará o valor de retorno `execAtPriority` .

#### Exemplo

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

### getCurrentPriority 
Retorna a prioridade contextual atual.

```javascript
var retval = MSApp.getCurrentPriority();
```

#### Parâmetros
Nenhuma. 

#### Valor de retorno
|Tipo | Descrição |
|:---- |:--- |
|DOMString | O valor de retorno é uma das cadeias de caracteres `MSApp.HIGH` , `MSApp.NORMAL` ou `MSApp.IDLE` .

#### Comentários
Esse método retorna a prioridade contextual atual (consulte [`MSApp Constants`](#msapp-constants) ), que pode ser alterada via `execAtPriority` and `execAsyncAtPriority` .

#### Exemplo

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### getHtmlPrintDocumentSource  

API síncrona que foi preterida. Para o Windows 10, consulte `getHtmlPrintDocumentSourceAsync` . Para aplicativos do Windows 8 e do 8,1, consulte a entrada MSDN para [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync
Retorna o conteúdo de origem que será impresso.

#### Parâmetros
`htmlDoc` no

|Tipo | Descrição |
|:---- |:--- |
|Documento | O documento HTML a ser impresso. Pode ser o documento raiz, o documento em um iframe, um fragmento de documento ou um documento SVG. Lembre-se de que htmlDoc deve ser um documento, não um elemento.

#### Exemplo 1

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

#### Exemplo 2

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

### getviewid 
Suporte para várias janelas. 

> [!NOTE] 
> Nos aplicativos UWP do JavaScript do Win 8.1, há suporte para várias janelas usando APIs DOM do MSApp que agora são depricated. Para Windows 10, use `window.open` , `window` e o novo `MSApp.getViewId` .

| Descrição |Windows 10 | Windows 8.1 |  
|:---- |:---- |:--- |  
| Criar nova janela | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|Novo objeto Window | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### Parâmetros
`window`

|Tipo | Descrição |
|:---- |:--- |
|DOMString | Um objeto que representa uma janela que contém um documento DOM. | 

#### Valor de retorno

`viewId`

|Tipo | Descrição |
|:---- |:--- |
|Número | Pode ser usado com várias [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs. 

#### Comentários
Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) e [`window`](https://developer.mozilla.org/docs/Web/API/Window) para criar novas janelas, mas então para interagir com APIs do WinRT, adicione a `MSApp.getViewId` API. Ele leva um `window` objeto como um parâmetro e retorna um `viewId` número que pode ser usado com várias [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs. 

##### Atraso na visibilidade 
Os modos de exibição do WinRT normalmente são iniciados e o desenvolvedor final usa algo como `TryShowAsStandaloneAsync` para exibir o modo de exibição quando ele está totalmente preparado. No mundo da Web, `window.open` mostra uma janela imediatamente e o usuário final pode assistir à medida que o conteúdo é carregado e renderizado. Para que seus novos modos de exibição do Windows atuem como modos de exibição no WinRT e não sejam exibidos imediatamente, adicionamos uma `window.open` opção. Por exemplo:
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### Diferenças da janela principal
A janela principal que é aberta inicialmente pelo sistema operacional funciona de forma diferente das janelas secundárias que ele abre: 

|Descrição | Primário | Secundária |
|:---- |:--- |:--- |
|Window. Open | Permitido | Não permitido |
|Window. Close | Fechar aplicativo | Fechar a janela |
| Restrições de navegação | ACUR apenas | Sem restrições |

A restrição para não permitir que janelas secundárias abertas pode mudar no futuro, dependendo do [Comentário](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).

##### Restrições de comunicação de mesma origem 
Há um problema técnico difícil que impede o suporte adequado a chamadas síncronas de mesma origem, de janela cruzada e de script. Quando você abre uma janela que é mesma origem, o script em uma janela tem permissão para chamar as funções diretamente na outra janela, e algumas dessas chamadas falharão. `postMessage` as chamadas funcionam muito bem e são a maneira recomendada de fazer coisas, se possível. O trabalho para melhorar esse problema está em andamento.


### isTaskScheduledAtPriorityOrHigher 
Retorna um valor booliano que indica se há trabalho pendente no nível de prioridade fornecido ou superior.

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### Parâmetros
`priority` no

|Tipo | Descrição |
|:---- |:--- |
|DOMString | Um valor de prioridade (consulte [constantes MSApp](#msapp-constants)) especificando o nível de prioridade e acima para consultar qualquer trabalho pendente na fila.

#### Valor de retorno
|Tipo | Descrição |
|:---- |:--- |
|Booliano | Retorna `true` se houver algum trabalho em fila no nível de prioridade especificado ou acima, `false` caso contrário.

#### Comentários
O `isTaskScheduledAtPriorityOrHigher` método fornece um meio para o código JavaScript determinar se há trabalho pendente nos vários níveis de prioridade (ou acima), com a intenção de que o código JavaScript de chamada possa decidir gerar um trabalho de prioridade mais alta.

#### Exemplo

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

### pageHandlesAllApplicationActivations
Usado para evitar uma atualização do caminho inicial (recarregamento de página) antes de cada evento de ativação (IE. clique em uma notificação ou em um bloco fixado). 

#### Parâmetros

|Tipo | Descrição |
|:---- |:--- |
Booliano | Use `MSApp.pageHandlesAllApplicationActivations(true)` para sempre ignorar a atualização do caminho de início (recarregar página) e, em vez disso, saltar diretamente para acionar o `WebUIApplication` evento ativado. Requer que todas as páginas manipulem eventos de ativação separadamente. Ao definir esse método como `true` , clicar em um evento ativado (como um notificaiton) não disparará o recarregamento, um essencial para aplicativos de uma única página que desejam evitar recarregamentos de página.

#### Exemplo 

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

### suppressSubdownloadCredentialPrompts 
Controla se um aplicativo suprime possíveis prompts de autenticação durante o download de recursos.

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### Parâmetros
`suppress` no

|Tipo | Descrição |
|:---- |:--- |
|Booliano | Um valor de true suprime os prompts de autenticação potencial. Um valor false não elimina qualquer prompt de autenticação potencial do usuário.

#### Valor de Returan
Nenhuma.

#### Comentários
O `suppressSubdownloadCredentialPrompts` método controla se um aplicativo suprime solicitações de autenticação potenciais durante o download de recursos. O comportamento padrão é não suprimir avisos de credenciais.

`suppressSubdownloadCredentialPrompts` destina-se ao uso por aplicativos que podem carregar um número excessivo de recursos que exigem autenticação, como um aplicativo de email (que pode conter um boletim informativo contendo várias imagens em que cada imagem requer autenticação).

Ao suprimir avisos de credenciais, as caixas de diálogo para autenticação em servidores não serão mostradas ao acessar recursos que exigem autenticação, e o recurso não será baixado. Observe que `suppressSubdownloadCredentialPrompts` não afeta outros prompts possíveis, como autenticação de proxy ou solicitação de certificação de cliente, nem afeta o XHR.

Lembre-se de que `suppressSubdownloadCredentialPrompts` impacta todo o conteúdo do aplicativo, incluindo o conteúdo hospedado no `webview` elemento.
 
**Importante:**  As decisões do prompt de credenciais são armazenadas em cache. Portanto, ao suprimir as solicitações de credenciais entrarão em vigor imediatamente, permitir solicitações de credenciais após supressão delas poderá precisar de um recarregamento do documento para entrar em vigor.

#### Exemplo

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### terminateApp
Termina o aplicativo atual e gera um relatório de falhas. 

```javascript
MSApp.terminateApp(error); 
```

#### Parâmetros
`error` no

Tipo | Descrição |
|:---- |:--- |
|Erro | Um `Error` objeto que você pode usar para descrever o erro que disparou o cancelamento. O `Error` objeto deve conter as propriedades Number, Description e Stack; um relatório de falha não será gerado se o objeto não contiver essas propriedades.

#### Valor de retorno
Nenhuma.

#### Comentários
Se o problema relatado `terminateApp` se tornar um dos cinco principais problemas do seu aplicativo, ele será exibido na página de qualidade do aplicativo.

#### Exemplo
Este exemplo chama `terminateApp` quando uma exceção é encontrada. Ele usa o `Error` objeto fornecido quando você captura uma exceção. 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### Constantes MSApp
Valores de prioridade permitidos associados a `execAsyncAtPriority` , `execAtPriority` , `getCurrentPriority` e `isTaskScheduldAtPriorityOrHigher` .

#### Atual
`current`

|Tipo | Descrição |
|:---- |:--- |
|DOMString | Quando `current` usado com o método apropriado (consulte também a seção), o método usará a prioridade contextual atual ao executar a operação solicitada.

#### Alto
`high`

|Tipo | Descrição |
|:---- |:--- |
|DOMString | Quando `high` usado com o método apropriado (consulte também a seção), o método usará maior prioridade normal ao executar a operação solicitada e enviará a operação antes de qualquer trabalho normal de prioridade existente.

#### Ocioso
`idle`

|Tipo | Descrição |
|:---- |:--- |
|DOMString | Quando `ideal` é usado com o método apropriado (consulte também a seção), o método usará a prioridade mais baixa do que o normal ao executar a operação solicitada e enviará a operação após qualquer trabalho normal de prioridade existente.

#### Normal
`normal`

|Tipo | Descrição |
|:---- |:--- |
|DOMString | Quando `normal` usado com o método apropriado (consulte também a seção), o método usará a prioridade existente normal ao executar a operação solicitada.

#### Exemplo

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### Requisitos
|IDL | Mshtml. idl |
|:---- |:--- |

## MSAppAsyncOperation

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### start
Inicia o `MSAppAsyncOperation` .

```javascript
var retval = MSAppAsyncOperation.start();
```

#### Parâmetros
Nenhuma.

#### Valor de retorno
Nenhuma.

#### Propriedades
`error` folha

|Tipo | Descrição |
|:---- |:--- |
|DOMError | Representa um erro em `MSAppAsyncOperation` .

```javascript
p = object.error
```

`oncomplete` folha

|Tipo | Descrição |
|:---- |:--- |
|EventHandler | Propriedade para definir um manipulador de eventos na conclusão de `MSAppAsyncOperation` .

```javascript
p = object.oncomplete
```

`onerror` folha

|Tipo | Descrição |
|:---- |:--- |
|EventHandler | Propriedade para definir um manipulador de eventos em um erro durante `MSAppAsyncOperation` .

```javascript
p = object.onerror
```

`readyState` folha

|Tipo | Descrição |
|:---- |:--- |
|Número | Representa o estado da operação assíncrona dentro do aplicativo do Windows usando JavaScript. Os valores incluem: iniciado [0], concluído [1], erro [2].

```javascript
p = object.readyState
```

`result` folha

|Tipo | Descrição |
|:---- |:--- |
|Qualquer |Representa o resultado de `MSAppAsyncOperation` .

```javascript
p = object.result
```
