---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. WPF. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. WPF. WebView2
ms.openlocfilehash: 2dd7bf1035cf5254f4668070d56d2bd2405f1276
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880259"
---
# Classe Microsoft. Web. WebView2. WPF. WebView2 

Namespace: Microsoft. Web. WebView2. WPF \
Assembly: Microsoft.Web.WebView2.Wpf.dll

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

Um controle para inserir conteúdo da Web em um aplicativo WPF.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | Um wrapper em torno do evento CoreWebView2. ContentLoading de CoreWebView2.
[CoreWebView2Ready](#corewebview2ready) | Esse evento é acionado quando o CoreWebView2 do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.
[NavigationCompleted](#navigationcompleted) | Um wrapper em torno do evento CoreWebView2. NavigationCompleted de CoreWebView2.
[NavigationStarting](#navigationstarting) | Um wrapper em torno do evento CoreWebView2. NavigationStarting de CoreWebView2.
[SourceChanged](#sourcechanged) | Um wrapper em torno do evento CoreWebView2. SourceChanged de CoreWebView2.
[WebMessageReceived](#webmessagereceived) | Um wrapper em torno do evento CoreWebView2. WebMessageReceived de CoreWebView2.
[CanGoBack](#cangoback) | Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.
[CanGoForward](#cangoforward) | Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.
[CoreWebView2](#corewebview2) | Acesse a funcionalidade completa da API Core. CoreWebView2 COM subjacente.
[Creationproperties](#creationproperties) | Obtém ou define um conjunto de opções que são usadas durante a inicialização do CoreWebView2 do controle.
[Origem](#source) | O URI de nível superior que o WebView está exibindo no momento (ou será exibido quando a inicialização de seu CoreWebView2 estiver concluída).
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Disparar explicitamente a inicialização do CoreWebView2 do controle.
[ExecuteScriptAsync](#executescriptasync) | Executa o código JavaScript do parâmetro javaScript no documento de nível superior atual renderizado no WebView.
[GoBack](#goback) | Navega o WebView para a página anterior no histórico de navegação.
[GoForward](#goforward) | Navega o WebView para a próxima página no histórico de navegação.
[NavigateToString](#navigatetostring) | Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.
[Recarregar](#reload) | Recarrega a página atual.
[Parar](#stop) | Interrompe todas as navegações e buscas de recursos pendentes.
[WebView2](#webview2) | Cria uma nova instância de um controle WebView2.

Esse controle é efetivamente um wrapper em torno da API COM WebView2, à qual você pode encontrar a documentação aqui: [https://aka.ms/webview2](https://aka.ms/webview2) você pode acessar diretamente a interface ICoreWebView2 subjacente e todas as suas funcionalidades acessando a propriedade CoreWebView2. Alguns dos recursos COM mais comuns também podem ser acessados diretamente por meio de métodos/Propriedades/eventos de wrapper no controle.

Após a criação, a propriedade CoreWebView2 do controle será nula. Isso ocorre porque a criação do CoreWebView2 é uma operação cara que envolve itens como iniciar processos do navegador Edge. Há duas maneiras de fazer com que o CoreWebView2 seja criado: 1) chame o método EnsureCoreWebView2Async. Isso é conhecido como inicialização explícita. 2) defina a propriedade Source (que pode ser feita a partir de marcações, por exemplo). Isso é conhecido como inicialização implícita. Qualquer uma das opções iniciará a inicialização em segundo plano e retornará para o chamador sem esperar que ele seja concluído. Para especificar as opções em relação ao processo de inicialização, passe seu próprio CoreWebView2Environment para EnsureCoreWebView2Async ou defina a propriedade Creationproperties do controle antes da inicialização.

Quando a inicialização terminar (independentemente de como foi disparada), os seguintes itens ocorrerão, nesta ordem: 1) o evento CoreWebView2Ready do controle será invocado. Se você precisar executar operações de configuração únicas no CoreWebView2 antes de seu uso, você deve fazer isso em um manipulador para esse evento. 2) se um URI tiver sido definido como a propriedade de origem, o controle começará a navegar para ele em segundo plano (isto é, essas etapas continuarão sem esperar a conclusão da navegação). 3) a tarefa retornada de EnsureCoreWebView2Async será concluída.

Para obter mais detalhes sobre qualquer um dos métodos/Propriedades/eventos envolvidos no processo de inicialização, consulte a documentação específica.

Como o CoreWebView2 do controle é um objeto muito pesado (possivelmente responsável por vários processos em execução e megabytes de espaço em disco), o controle implementa IDisposable para fornecer um meio explícito para liberá-lo. Chamar Dispose vai liberar o CoreWebView2 e seus recursos subjacentes (exceto os que também estão sendo usados por outras exibições) e redefinir CoreWebView2 como NULL. Após Dispose ter sido chamado, o CoreWebView2 não pode ser reinicializado e qualquer tentativa de usar a funcionalidade que o exige será gerar um ObjectDisposedException.

Observe que esse controle estende HwndHost para inserir janelas que residem fora do ecossistema do WPF. Isso tem algumas implicações em relação ao comportamento de entrada e saída do controle, bem como a funcionalidade que "herda" de UIElement e FrameworkElement. Consulte a documentação de interoperabilidade do HwndHost e do WPF/Win32 para obter mais informações:

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## Parte

#### ContentLoading 

Um wrapper em torno do evento CoreWebView2. ContentLoading de CoreWebView2.

> < do evento público EventHandler CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

A única diferença entre esse evento e CoreWebView2. ContentLoading é o primeiro parâmetro que é passado para manipuladores. Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. ContentLoading receberão a instância CoreWebView2.

#### CoreWebView2Ready 

Esse evento é acionado quando o CoreWebView2 do controle termina de ser inicializado (independentemente de como a inicialização foi disparada), mas antes de ser usado para qualquer coisa.

> evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Você deve tratar esse evento se precisar executar operações de configuração únicas no CoreWebView2 que você deseja afetar todos os seus usos (por exemplo, adicionar manipuladores de eventos, definir configurações, instalar scripts de criação de documentos, adicionar objetos host). Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.

Esse evento não fornece argumentos, e o remetente será o controle WebView2, cuja propriedade CoreWebView2 agora será válida (ou seja, não nula) pela primeira vez.

#### NavigationCompleted 

Um wrapper em torno do evento CoreWebView2. NavigationCompleted de CoreWebView2.

> < do evento público EventHandler CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

A única diferença entre esse evento e CoreWebView2. NavigationCompleted é o primeiro parâmetro que é passado para manipuladores. Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. NavigationCompleted receberão a instância CoreWebView2.

#### NavigationStarting 

Um wrapper em torno do evento CoreWebView2. NavigationStarting de CoreWebView2.

> < do evento público EventHandler CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

A única diferença entre esse evento e CoreWebView2. NavigationStarting é o primeiro parâmetro que é passado para manipuladores. Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. NavigationStarting receberão a instância CoreWebView2.

#### SourceChanged 

Um wrapper em torno do evento CoreWebView2. SourceChanged de CoreWebView2.

> evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

A única diferença entre esse evento e CoreWebView2. SourceChanged é o primeiro parâmetro que é passado para manipuladores. Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. SourceChanged receberão a instância CoreWebView2.

#### WebMessageReceived 

Um wrapper em torno do evento CoreWebView2. WebMessageReceived de CoreWebView2.

> < do evento público EventHandler CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

A única diferença entre esse evento e CoreWebView2. WebMessageReceived é o primeiro parâmetro que é passado para manipuladores. Manipuladores desse evento receberão o controle WebView2, enquanto manipuladores de CoreWebView2. WebMessageReceived receberão a instância CoreWebView2.

#### CanGoBack 

Retorna verdadeiro se a WebView pode navegar para uma página anterior no histórico de navegação.

> bool público [CanGoBack](#cangoback)

Wrapper em torno da propriedade CoreWebView2. CanGoBack de CoreWebView2. Se CoreWebView2 ainda não for inicializado, retornará false.

#### CanGoForward 

Retorna verdadeiro se a WebView pode navegar para uma próxima página no histórico de navegação.

> Public bool [CanGoForward](#cangoforward)

Wrapper ao meio da propriedade CoreWebView2. CanGoForward de CoreWebView2. Se CoreWebView2 ainda não for inicializado, retornará false.

#### CoreWebView2 

Acesse a funcionalidade completa da API Core. CoreWebView2 COM subjacente.

> CoreWebView2 público [CoreWebView2](#corewebview2)

Retorna NULL até que a inicialização seja concluída. Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.

##### Exceções
* `InvalidOperationException` Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário). Consulte DispatcherObject. VerifyAccess para obter mais informações.

* `ObjectDisposedException` Lançada se Dispose já tiver sido chamado no controle.

#### Creationproperties 

Obtém ou define um conjunto de opções que são usadas durante a inicialização do CoreWebView2 do controle.

> [criação](#creationproperties) de CoreWebView2CreationProperties público

A configuração dessa propriedade não funcionará depois que a inicialização do CoreWebView2 do controle tiver começado (o valor antigo será mantido). Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.

#### Origem 

O URI de nível superior que o WebView está exibindo no momento (ou será exibido quando a inicialização de seu CoreWebView2 estiver concluída).

> [fonte](#source) de URI público

Em geral, obter essa propriedade equivale a obter a propriedade CoreWebView2. Source de CoreWebView2 e definir essa propriedade equivale a chamar o método CoreWebView2. Navigate em CoreWebView2. Obter essa propriedade antes da inicialização do CoreWebView2 será recuperar o último URI que estava definido. A configuração dessa propriedade antes da inicialização do CoreWebView2 fará com que a inicialização comece em segundo plano (se ainda não estiver em andamento), após a qual o WebView2 navegará até o URI especificado. Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.

##### Exceções
* `ObjectDisposedException` Lançada se Dispose já tiver sido chamado no controle.

#### EnsureCoreWebView2Async 

Disparar explicitamente a inicialização do CoreWebView2 do controle.

> [EnsureCoreWebView2Async](#ensurecorewebview2async)de tarefas públicas (ambiente CoreWebView2Environment)

Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.

##### Parâmetros
* `environment` Um CoreWebView2Environment pré-criado que deve ser usado para criar o CoreWebView2. Criar seu próprio ambiente permite que você controle várias opções que afetam como a CoreWebView2 é inicializada. Se você passar um ambiente para esse método, ele substituirá as configurações especificadas na propriedade Creationproperties. Se você passar NULL (o valor padrão) e nenhum valor tiver sido definido como Creationproperties, um ambiente padrão será criado e usado automaticamente. 

##### Devolver
Uma tarefa que representa o processo de inicialização em segundo plano. Quando a tarefa for concluída, a propriedade CoreWebView2 estará disponível para uso (ou seja, não nulo). Observe que o evento CoreWebView2Ready do controle será invocado antes da conclusão da tarefa. 

Chamar esse método momentos adicionais não terão efeito (qualquer ambiente especificado será ignorado) e retornará a mesma tarefa que a primeira chamada. Chamar esse método após a inicialização foi disparada implicitamente, definindo a propriedade Source não terá nenhum efeito (qualquer ambiente especificado é ignorado) e simplesmente retornar uma tarefa representando essa inicialização já em andamento. Observe que, embora esse método seja assíncrono e retorne uma tarefa, ele ainda deve ser chamado no thread da interface do usuário, como a maioria das funcionalidades públicas da maioria dos controles da interface do usuário. 

##### Exceções
* `InvalidOperationException` Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário). Consulte DispatcherObject. VerifyAccess para obter mais informações.

* `ObjectDisposedException` Lançada se Dispose já tiver sido chamado no controle.

#### ExecuteScriptAsync 

Executa o código JavaScript do parâmetro javaScript no documento de nível superior atual renderizado no WebView.

> Cadeia de caracteres de< de tarefas assíncronas pública > [ExecuteScriptAsync](#executescriptasync)(cadeia de caracteres JavaScript)

Equivalente a chamadas CoreWebView2.ExecuteScriptAsync no CoreWebView2

##### Exceções
* `InvalidOperationException` Gerado se CoreWebView2 ainda não foi inicializado.

* `InvalidOperationException` Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário). Consulte DispatcherObject. VerifyAccess para obter mais informações.

* `ObjectDisposedException` Lançada se Dispose já tiver sido chamado no controle.

#### GoBack 

Navega o WebView para a página anterior no histórico de navegação.

> public void [(](#goback)) public void

Equivalente a chamar CoreWebView2. GoBack no CoreWebView2 se CoreWebView2 ainda não tiver sido inicializado, não fará nada.

##### Exceções
* `InvalidOperationException` Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário). Consulte DispatcherObject. VerifyAccess para obter mais informações.

* `ObjectDisposedException` Lançada se Dispose já tiver sido chamado no controle.

#### GoForward 

Navega o WebView para a próxima página no histórico de navegação.

> public void [GoForward](#goforward)()

Equivalente a chamar CoreWebView2. GoForward em CoreWebView2 se CoreWebView2 ainda não foi inicializado, não faz nada.

##### Exceções
* `InvalidOperationException` Lançada se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário). Consulte DispatcherObject. VerifyAccess para obter mais informações.

* `ObjectDisposedException` Lançada se Dispose já tiver sido chamado no controle.

#### NavigateToString 

Inicia uma navegação para htmlContent como código-fonte HTML de um novo documento.

> public void [NavigateToString](#navigatetostring)(cadeia de caracteres htmlContent)

Equivalente a chamar CoreWebView2. NavigateToString no CoreWebView2

##### Exceções
* `InvalidOperationException` Gerado se CoreWebView2 ainda não foi inicializado.

" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).  Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.

#### Recarregar 

Recarrega a página atual.

> recarregamento [Reload](#reload)nulo público ()

Equivalente a chamar CoreWebView2. reload no CoreWebView2

##### Exceções
* `InvalidOperationException` Gerado se CoreWebView2 ainda não foi inicializado.

" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).  Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.

#### Parar 

Interrompe todas as navegações e buscas de recursos pendentes.

> [Stop](#stop)void Public ()

Equivalente a chamar CoreWebView2. Stop no CoreWebView2

##### Exceções
* `InvalidOperationException` Gerado se CoreWebView2 ainda não foi inicializado.

" <exception cref="InvalidOperationException"> Acionado se o thread de chamada não for o thread que criou esse objeto (geralmente o thread da interface do usuário).  Consulte DispatcherObject. VerifyAccess para obter mais informações. </exception>
<exception cref="ObjectDisposedException"> Lançada se Dispose já tiver sido chamado no controle.

#### WebView2 

Cria uma nova instância de um controle WebView2.

> [WebView2](#webview2)público ()

Observe que o CoreWebView2 do controle será nulo até ser inicializado. Consulte a documentação da classe WebView2 para obter uma visão geral de inicialização.

