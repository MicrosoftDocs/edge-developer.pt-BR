---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. WinForms. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. WinForms. WebView2
ms.openlocfilehash: 7d707c2a6ecb8127074735f06ba6d4f1f28eea0c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879447"
---
# Classe Microsoft. Web. WebView2. WinForms. WebView2 

Namespace: Microsoft. Web. WebView2. WinForms \
Assembly: Microsoft.Web.WebView2.WinForms.dll

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

Controle para inserir WebView2 em WinForms.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | ContentLoading despachos quando uma navegação começa a ser um novo URI e o conteúdo desse URI começa a ser renderizado.
[CoreWebView2Ready](#corewebview2ready) | Esse evento é acionado quando o [CoreWebView2](#corewebview2) do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.
[NavigationCompleted](#navigationcompleted) | O NavigationCompleted despacha após uma navegação do documento de nível superior executa a renderização com êxito ou não.
[NavigationStarting](#navigationstarting) | O NavigationStarting despacha antes de uma nova navegação começar para o documento de nível superior do WebView2.
[SourceChanged](#sourcechanged) | Os despachos SourceChanged após a alteração da propriedade de origem.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived despachos após conteúdo da Web envia uma mensagem para o host do aplicativo via `chrome.webview.postMessage` .
[CoreWebView2](#corewebview2) | O CoreWebView2 subjacente.
[Origem](#source) | A propriedade Source é o URI do documento de nível superior do WebView2.
[ZoomFactor](#zoomfactor) | O fator de zoom para o WebView.
[CanGoBack](#cangoback) | Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação por meio do método GoBack.
[CanGoForward](#cangoforward) | Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação por meio do método GoForward.
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Disparar explicitamente a inicialização do [CoreWebView2](#corewebview2)do controle.
[ExecuteScriptAsync](#executescriptasync) | Executa o script fornecido no documento de nível superior do WebView2.
[GoBack](#goback) | Navegar para a página anterior no histórico de navegação.
[GoForward](#goforward) | Navegar para a próxima página no histórico de navegação.
[NavigateToString](#navigatetostring) | Renderize o HTML fornecido como o documento de nível superior do WebView2.
[Recarregar](#reload) | Recarregue o documento de nível superior da WebView2.
[Parar](#stop) | Parar a navegação em andamento no WebView2.
[WebView2](#webview2) | Crie um novo controle WinForms do WebView2.

## Parte

#### ContentLoading 

ContentLoading despachos quando uma navegação começa a ser um novo URI e o conteúdo desse URI começa a ser renderizado.

> < do evento público EventHandler CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

Isso equivale ao evento ContentLoading no CoreWebView2. Consulte a documentação do CoreWebView2. ContentLoading para obter mais informações.

#### CoreWebView2Ready 

Esse evento é acionado quando o [CoreWebView2](#corewebview2) do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.

> evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Você deve tratar esse evento se precisar executar operações de configuração únicas no CoreWebView2 que você deseja afetar todos os seus usos (por exemplo, adicionar manipuladores de eventos, definir configurações, instalar scripts de criação de documentos, adicionar objetos host).

Esse evento não fornece argumentos, e o remetente será o controle WebView2, cuja propriedade CoreWebView2 agora será válida (ou seja, não nula) pela primeira vez.

#### NavigationCompleted 

O NavigationCompleted despacha após uma navegação do documento de nível superior executa a renderização com êxito ou não.

> < do evento público EventHandler CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

Isso equivale ao evento NavigationCompleted no CoreWebView2. Consulte a documentação do CoreWebView2. NavigationCompleted para obter mais informações.

#### NavigationStarting 

O NavigationStarting despacha antes de uma nova navegação começar para o documento de nível superior do WebView2.

> < do evento público EventHandler CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

Isso equivale ao evento NavigationStarting no CoreWebView2. Consulte a documentação do CoreWebView2. NavigationStarting para obter mais informações.

#### SourceChanged 

Os despachos SourceChanged após a alteração da propriedade de origem.

> evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

Isso pode ocorrer durante uma navegação ou, caso contrário, o script na página alterará o URI do documento. Isso equivale ao evento SourceChanged no CoreWebView2. Consulte documentação da CoreWebView2. SourceChanged para obter mais informações.

#### WebMessageReceived 

WebMessageReceived despachos após conteúdo da Web envia uma mensagem para o host do aplicativo via `chrome.webview.postMessage` .

> < do evento público EventHandler CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

Isso equivale ao evento WebMessageReceived no CoreWebView2. Consulte a documentação do CoreWebView2. WebMessageReceived para obter mais informações.

#### CoreWebView2 

O CoreWebView2 subjacente.

> CoreWebView2 público [CoreWebView2](#corewebview2)

Use essa propriedade para executar mais operações no conteúdo do WebView2 do que é exposto no WebView2. Esse valor é nulo até ser inicializado. Você pode forçar o CoreWebView2 subjacente a inicializar por meio do método InitializeAsync.

#### Origem 

A propriedade Source é o URI do documento de nível superior do WebView2.

> [fonte](#source) de URI público

A configuração da fonte equivale a chamar CoreWebView2. Navigate. Se a CoreWebView2 subjacente ainda não tiver sido inicializada, essa propriedade será "About: blank". Se a propriedade estiver definida como um URI não absoluto ou nulo, a propriedade permanecerá inalterada. Consulte CoreWebView2. Navegue na documentação para obter mais informações.

#### ZoomFactor 

O fator de zoom para o WebView.

> [ZoomFactors](#zoomfactor) duplos públicos

#### CanGoBack 

Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação por meio do método GoBack.

> bool público [CanGoBack](#cangoback)

Isso equivale à propriedade CanGoBack no CoreWebView2. Se a CoreWebView2 subjacente ainda não tiver sido inicializada, essa propriedade será falsa. Consulte a documentação do CoreWebView2. CanGoBack para obter mais informações.

#### CanGoForward 

Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação por meio do método GoForward.

> Public bool [CanGoForward](#cangoforward)

Isso equivale à propriedade CanGoForward no CoreWebView2. Se a CoreWebView2 subjacente ainda não tiver sido inicializada, essa propriedade será falsa. Consulte a documentação do CoreWebView2. CanGoForward para obter mais informações.

#### EnsureCoreWebView2Async 

Disparar explicitamente a inicialização do [CoreWebView2](#corewebview2)do controle.

> [EnsureCoreWebView2Async](#ensurecorewebview2async)de tarefas públicas (ambiente CoreWebView2Environment)

##### Parâmetros
* `environment` Um CoreWebView2Environment pré-criado que deve ser usado para criar o CoreWebView2. Criar seu próprio ambiente permite que você controle várias opções que afetam como a CoreWebView2 é inicializada. Se você passar NULL (o valor padrão), um ambiente padrão será criado e usado automaticamente. 

##### Devolver
Uma tarefa que representa o processo de inicialização em segundo plano. Quando a tarefa for concluída, a propriedade CoreWebView2 estará disponível para uso (ou seja, não nulo). Observe que o evento [CoreWebView2Ready](#corewebview2ready) do controle será invocado antes da conclusão da tarefa. 

Chamar esse método momentos adicionais não terão efeito (qualquer ambiente especificado será ignorado) e retornará a mesma tarefa que a primeira chamada. Chamar esse método após a inicialização foi disparada implicitamente, definindo a propriedade [Source](#source) não terá nenhum efeito (qualquer ambiente especificado é ignorado) e simplesmente retornar uma tarefa representando essa inicialização já em andamento. 

##### Exceções
* `System.InvalidOperationException` Lançada quando invocada do thread que não é da interface do usuário.

#### ExecuteScriptAsync 

Executa o script fornecido no documento de nível superior do WebView2.

> Cadeia de caracteres de< de tarefa assíncrona pública > [ExecuteScriptAsync](#executescriptasync)(script de cadeia de caracteres)

Isso equivale ao método ExecuteScriptAsync no CoreWebView2. Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método lançará um InvalidOperationException. Consulte CoreWebView2.Exedocumentação do cuteScriptAsync para obter mais informações.

#### GoBack 

Navegar para a página anterior no histórico de navegação.

> public void [(](#goback)) public void

Isso equivale ao método GoBack no CoreWebView2. Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método não fará nada. Consulte a documentação do CoreWebView2. GoBack para obter mais informações.

#### GoForward 

Navegar para a próxima página no histórico de navegação.

> public void [GoForward](#goforward)()

Isso equivale ao método GoForward no CoreWebView2. Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método não fará nada. Consulte a documentação do CoreWebView2. GoForward para obter mais informações.

#### NavigateToString 

Renderize o HTML fornecido como o documento de nível superior do WebView2.

> public void [NavigateToString](#navigatetostring)(cadeia de caracteres htmlContent)

Isso equivale ao método NavigateToString no CoreWebView2. Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método lançará um InvalidOperationException. Consulte a documentação do CoreWebView2. NavigateToString para obter mais informações.

#### Recarregar 

Recarregue o documento de nível superior da WebView2.

> recarregamento [Reload](#reload)nulo público ()

Isso equivale ao método reload no CoreWebView2. Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método lançará um InvalidOperationException. Consulte CoreWebView2. recarregue a documentação para obter mais informações.

#### Parar 

Parar a navegação em andamento no WebView2.

> [Stop](#stop)void Public ()

Isso equivale ao método Stop no CoreWebView2. Se o CoreWebView2 subjacente ainda não tiver sido inicializado, esse método não fará nada. Consulte CoreWebView2. pare a documentação para obter mais informações.

#### WebView2 

Crie um novo controle WinForms do WebView2.

> [WebView2](#webview2)público ()

Após a construção, a propriedade CoreWebView2 é NULL. Chame [EnsureCoreWebView2Async](#ensurecorewebview2async) para inicializar o CoreWebView2 subjacente.

