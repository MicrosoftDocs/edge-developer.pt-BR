---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle Microsoft Edge WebView 2
title: Notas de versão do Microsoft Edge WebView2 para Win32, WPF e WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 14030d3dde8c4e68c0790073dc38e5c856e2a091
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652746"
---
# Notas de versão do SDK do WebView2  

Notas de versão do [SDK do WebView2][WebView2NuGetGallery].  

## 0.9.515-pré-lançamento

[Pacote NuGet][WebView2NuGetGallery0.9.515-prerelease] | versão mínima do Microsoft Edge 84.0.515.0.

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

* **Lançamento:** O WebView2 agora é compatível com Windows Forms e WPF no .NET Framework 4.6.2 ou posterior e .NET Core 3,0 ou posterior no **pacote de pré-lançamento**
* Fazer check-out do [Guia de introdução do WPF](./gettingstarted/wpf.md) para começar a criar aplicativos WPF e nossa referência do [WPF](./reference/wpf/0-9-515-reference-webview2.md) para APIs específicas do WPF
* Fazer checkout do [Guia de introdução do Windows Forms](./gettingstarted/winforms.md) para começar a criar aplicativos do Windows Forms e a [referência de formulários](./reference/winforms/0-9-515-reference-webview2.md) do Windows para APIs específicas do Windows Forms
* Fazer check-out da [referência .net](./reference/dotnet/0-9-515-reference-webview2.md) para APIs CoreWebView2
* **Problemas conhecidos:** Estamos cientes de alguns problemas nesta versão pré-lançamento que resolveremos em lançamentos futuros
  * **Reconhecimento de DPI:** No momento, o WebView2 para WPF não reconhece DPI. Ao inicializar o WebView2 em monitores High DPI, há um problema conhecido em que o WebView em primeiro inicializa como uma fração da janela até que a janela seja redimensionada.
  * **WPF Designer:** Esta versão não oferece suporte no momento ao designer do WPF. Colocar o controle WebView2 em seu aplicativo modificando diretamente o XAML apropriado em um editor de texto

## 0.9.488

[Pacote NuGet][WebView2NuGetGallery0.9.488] | versão mínima do Microsoft Edge 84.0.488.0.

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

* **Lançamento:** A partir da próxima versão do Microsoft Edge 83, o WebView sempre não direcionará mais o canal de navegador estável. Em vez disso, ele direcionará outro conjunto de binários, com a marca [Microsoft Edge WebView2 Runtime](./index.md#microsoft-edge-webview2-runtime), que pode ser instalada em cadeia por meio de um instalador que estamos desenvolvendo no momento. Mais detalhes na [distribuição de aplicativo](./index.md#app-distribution).
* **Lançamento:** Em frente, lançaremos dois pacotes: um pacote de pré-lançamento com APIs experimentais (para experimentar) e um pacote de lançamento estável com APIs estáveis (você pode depender delas). Desfaça checkout do [SDK do Microsoft Edge WebView2](./index.md#microsoft-edge-webview2-sdk) para saber mais sobre as diferenças.
* **Alteração de quebra:** Para garantir que nossa API se alinhe com as convenções de nomenclatura da API do Windows, atualizamos os nomes das seguintes interfaces:
  * CORE_WEBVIEW2_ * prefixo agora está COREWEBVIEW2_ *.
  * [GetCoreWebView2BrowserVersionInfo](reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo) agora é [GetAvailableCoreWebView2BrowserVersionString](reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring)
  * [get_BrowserVersionInfo](reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo) agora é [get_BrowserVersionString](reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring)
  * [Addremoteobject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) agora é [AddHostObjectToScript](reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript)
  * [RemoveRemoteObject](reference/win32/0-9-430/icorewebview2.md#removeremoteobject) agora é [RemoveHostObjectFromScript](reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript)
  * Chrome. WebView. remoteObjects agora é Chrome. WebView. hostObjects
* **Alteração de quebra:** Os métodos de proxy addremoteobject JS também foram renomeados.
  * getLocal agora é getlocalproperty
  * setlocal agora é setlocalproperty
  * GetRemote agora é gethostproperty
  * SetRemote agora é sethostproperty
  * applyRemote agora é applyHostFunction
* **Alteração de quebra:** o [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) agora está obsoleto e foi substituído pelo [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).  
* Evento [FrameNavigationCompleted](reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted) adicionado. Agora, quando um iframe concluir a navegação, um evento é acionado e retorna o sucesso da navegação e da ID de navegação.
* Foi adicionada uma interface [ICoreWebView2EnvironmentOptions](reference/win32/0-9-488/ICoreWebView2EnvironmentOptions.md) , que pode ser usada para determinar a versão do tempo de execução do WebView2 para a qual o aplicativo se destina.
* Adicionada a configuração [IsBuiltInErrorPageEnabled](reference/win32/0-9-488/ICoreWebView2Settings.md#get_isbuiltinerrorpageenabled) . Agora, você pode optar por habilitar ou desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.
* Injeção de objeto remoto atualizada para dar suporte a implementações de .NET IDispatch. ([#113](https://github.com/MicrosoftEdge/WebViewFeedback/issues/113))
* Evento [NewWindowRequested](reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested) atualizado para manipular solicitações de menus de contexto. ([#108](https://github.com/MicrosoftEdge/WebViewFeedback/issues/108))
* Lançou nosso primeiro pacote de pré-lançamento separado no qual você pode acessar APIs de hospedagem Visual. Atualizamos o [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) para incluir essas novas APIs experimentais.
  * Adicionada uma interface [ICoreWebView2ExperimentalCompositionController](reference/win32/0-9-488/ICoreWebView2ExperimentalCompositionController.md) , que é usada para se conectar a uma árvore de composição e fornecer a entrada para o WebView.
  * [ICoreWebView2ExperimentalPointerInfo](reference/win32/0-9-488/ICoreWebView2ExperimentalPointerInfo.md) adicionado que contém todas as informações de um POINTER_INFO. Ele é passado para SendPointerInput para injetar a entrada do ponteiro no WebView.
  * Adicionado [ICoreWebView2ExperimentalCursorChangedEventHandler](reference/win32/0-9-488/ICoreWebView2ExperimentalCursorChangedEventHandler.md) que informa ao aplicativo quando o cursor do mouse sobre a WebView deve ser alterado. Quando o mouse está sobre uma caixa de texto no WebView, o cursor muda da seta para o seletor. A propriedade cursor no CompositionController informa ao aplicativo qual o cursor do mouse deve estar no momento para o WebView.

## 0.9.430

[Pacote NuGet][WebView2NuGetGallery0.9.430] | versão mínima do Microsoft Edge 82.0.430.0.

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

Este SDK é a nossa versão do Win32 C++ beta oficial, que incorpora várias solicitações de recursos que recebemos. Tentamos limitar o número de lançamentos com alterações significativas, mas à medida que nos aproximamos da nossa disponibilidade geral, estamos usando o nosso lançamento beta para incorporar várias grandes alterações de uma só vez.

* **Alteração de quebra:**  À medida que nos aproximamos do lançamento final, renomeamos o prefixo *IWebView2WebView* como *ICoreWebView2* para garantir que nossa API se alinhe com a Convenção de nomenclatura da API do Windows. Além disso, para tornar o SDK extensível para ser usado por estruturas de interface do usuário, separamos o ICoreWebView2 em [ICoreWebView2](reference/win32/0-9-430/icorewebview2.md) e [ICoreWebView2Host](reference/win32/0-9-430/icorewebview2host.md). O ICoreWebView2Host dá suporte ao redimensionamento, ao mostrar e ocultar, ao enfocar e a outras funcionalidades relacionadas à janela e composição. ICoreWebView2 dá suporte a todas as outras funcionalidades do WebView2. Para saber mais sobre como incorporar essas alterações, faça o check-out da nossa [solicitação pull](https://github.com/MicrosoftEdge/WebView2Samples/pull/17) em nosso projeto [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) .
* **Alteração de quebra:** Divida o [DocumentStateChanged](reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged) em três componentes: [SourceChanged](reference/win32/0-9-430/icorewebview2.md#add_sourcechanged), [ContentLoading](reference/win32/0-9-430/icorewebview2.md#add_contentloading)e [historychanged](reference/win32/0-9-430/icorewebview2.md#add_historychanged). Agora, quando a URL de origem muda o evento SourceChanged é acionado. Quando o estado do histórico é alterado, o evento Historychanged é acionado. O evento ContentLoading é acionado antes do script inicial quando um novo documento está sendo carregado.
* Suporte adicionado para a arquitetura ARM64
* Suporte do painel de entrada de software (SIP) adicionado para dispositivos de tela sensível ao toque
* Suporte adicional para `Windows Server 2008 R2` , `Windows Server 2012/2012 R2` e `Windows Server 2016`
* Adicionado [NotifyParentWindowPositionChanged](reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged) que permite que a barra de status siga a janela no modo de janela. Isso também precisará ser implementado no modo sem janelas para que os recursos de acessibilidade funcionem.
* Adicionada a configuração [AreRemoteObjectsAllowed](reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed) para controlar globalmente se uma página pode ser acessada por qualquer objeto remoto. Por padrão, o AreRemoteObjectsAllowed está habilitado, o que significa que os objetos remotos adicionados por [Addremoteobject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) podem ser acessados da página. Quando o AreRemoteObjectsAllowed estiver desabilitado, os objetos não poderão ser acessados da página. As alterações serão aplicadas no próximo evento de navegação.
* Adicionada a configuração [IsZoomControlEnabled](reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled) para impedir que os usuários afetem o zoom do uso da WebView `ctrl`  +  `+` / `-` ou da `ctrl` roda do mouse. O zoom ainda pode ser definido por meio de [put_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor) quando essa configuração estiver desabilitada.  
* ZoomFactor alterado para aplicar somente ao WebView atual. As alterações de zoom no WebView atual não afetam outros webviews que acontecem no mesmo local de origem. Consulte [get_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor) para obter mais detalhes.
* Interface de usuário ZoomView HID para WebView. ([#95](https://github.com/MicrosoftEdge/WebViewFeedback/issues/95))
* [SetBoundsAndZoomFactor](reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor)adicionado. Agora, você pode definir o fator de zoom e os limites de um WebView ao mesmo tempo.
* Evento [WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) adicionado. Consulte [add_WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) para obter mais detalhes. ([#119](https://github.com/MicrosoftEdge/WebViewFeedback/issues/119))
* Foi adicionado suporte para o tipo de caixa de diálogo beforeunload para eventos de caixa de diálogo JavaScript e adicionado [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD](reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind) entrada de enumeração.
* Adicionados [Getheaders](reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders) a HttpRequestHeaders, [GetHeader](reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader) para HttpResponseHeaders, e a propriedade [get_HasCurrentHeader](reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader) para HttpHeadersCollectionIterator.
* **Alteração de quebra:** Comportamento DevToolsProtocolEventReceived modificado. Agora, você pode criar um [DevToolsProtocolEventReceiver](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md) para um evento de protocolo de devtools específico e assinar/cancelar a assinatura para esse evento usando [add_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived) / [remove_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived).
* **Alteração de quebra:** Propriedade [get_WebMessageAsString](reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring) ' WebMessageReceivedEventArgs alterada para um método [TryGetWebMessageAsString](reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring) .
* **Alteração de quebra:** Método [HANDLE](reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle) ' AcceleratorKeyPressedEventArgs ' alterado para uma propriedade de [get_Handled](reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled) .

## 0.8.355

[Pacote NuGet][WebView2NuGetGallery0.8.355] | versão mínima do Microsoft Edge 80.0.355.0.

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

* Exemplo de WebView2API lançada-um guia abrangente de nosso SDK. Dê uma olhada [aqui](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample)!
* Suporte do IME adicionado para todos os idiomas além do inglês. ([#30](https://github.com/MicrosoftEdge/WebViewFeedback/issues/30))
* A superfície da API do evento WebResourceRequested em resposta a relatórios de erros.  A especificação simultânea de um filtro e um evento de criação já foi preterido.  Para criar um evento de recurso da Web solicitado, use [add_WebResourceRequested](reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested) para adicionar o evento e [AddWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter) para adicionar um filtro.  [RemoveWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter) remove o filtro.  ([#36](https://github.com/MicrosoftEdge/WebViewFeedback/issues/36)) ([#74](https://github.com/MicrosoftEdge/WebViewFeedback/issues/74))  
* **Alteração de quebra:**  Comportamento da tela inteira modificada. [IsFullScreenAllowed](reference/win32/0-8-190/IWebView2Settings.md#get_isfullscreenallowed_deprecated)preterido.  Agora, por padrão, se um elemento de uma WebView (como um vídeo) estiver definido como tela inteira, ele preenche os limites do WebView.  Use o evento [ContainsFullScreenElementChanged](reference/win32/0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md#interface-iwebview2containsfullscreenelementchangedeventhandler) e [get_ContainsFullScreenElement](reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement) para especificar como o aplicativo deve redimensionar o WebView se um elemento quiser entrar em modo de tela inteira.  

## 0.8.314

[Pacote NuGet][WebView2NuGetGallery0.8.314] | versão mínima do Microsoft Edge 80.0.314.0.

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

* Suporte adicional para Windows 7, Windows 8/8.1.
* Adicionado o suporte de depuração de código do Visual Studio e do Visual Studio para WebView2. Agora, você pode depurar o script no WebView2 diretamente do IDE. Clique [aqui](/microsoft-edge/hosting/webview2#debugging-webview2) para obter mais detalhes.  
* Adicionado `Native Object Injection` , que permite que o script em execução no WebView2 seja aprovado em um objeto IDispatch do componente Win32 do aplicativo e acesse as propriedades do objeto IDispatch.  Consulte [Addremoteobject](reference/win32/0-8-190/iwebview2webview4.md#addremoteobject) para obter mais detalhes.  ([#17](https://github.com/MicrosoftEdge/WebViewFeedback/issues/17)).  
* `AcceleratorKeyPressed`Evento adicionado.  Consulte [add_AcceleratorKeyPressed](reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed) para obter mais detalhes.  ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Desabilitado `Context Menus` .  Consulte [put_AreDefaultContextMenusEnabled](reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled) para obter mais detalhes ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Atualizado `DPI Awareness` . Agora, o reconhecimento de DPI da WebView será igual ao reconhecimento de DPI do aplicativo host. Observação se outro aplicativo híbrido for iniciado com um reconhecimento de DPI diferente do que o WebView original, o novo WebView não será iniciado se o diretório de dados do usuário for o mesmo ([#1](https://github.com/MicrosoftEdge/WebViewFeedback/issues/1)).
* Atualizado `Notification Change Behavior` para que o WebView2 rejeite automaticamente solicitações de permissão de notificação solicitadas pelo conteúdo da Web hospedado no WebView.

## 0.8.270  

[Pacote NuGet][WebView2NuGetGallery0.8.270] | versão mínima do Microsoft Edge 78.0.270.0.  

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

* Adicionado `DocumentTitleChanged` evento para indicar a mudança de título do documento \ ([\ #27][MicrosoftEdgeWebViewFeedbackIssue27]\).  
* `GetWebView2BrowserVersionInfo`API adicionada \ ([\ #18][MicrosoftEdgeWebViewFeedbackIssue18]\).  
* `NewWindowRequested`Evento adicionado.  
* `CreateWebView2EnvironmentWithDetails`Função updated a ser removida `releaseChannelPreference` .  Consulte a função [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] para obter mais detalhes.  Ainda há suporte para a substituição da variável de ambiente e do registro.  A preferência de canal padrão é usada, a menos que seja substituída.  
    Durante a pesquisa de canais, ignoramos qualquer versão de canal mais antiga que não seja compatível com o SDK do WebView2.  
    Selecionamos o canal mais estável para garantir os comportamentos mais consistentes para o usuário final.  Ao testar com as versões mais recentes do Canárias, você deve criar um script para definir a variável de ambiente `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` antes de iniciar o aplicativo.  
* `CreateWebView2EnvironmentWithDetails`Função updated com lógica para selecionar `userDataFolder` quando não especificado.  Consulte a função [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] para obter mais detalhes.  Se você usou anteriormente o `userDataFolder` local padrão, ao alternar para o novo SDK, o padrão `userDataFolder` será Reset (definido como um novo local no diretório de código do host) e seu estado também será redefinido.  
    Se o processo de host não tiver permissão para gravar no diretório especificado, `CreateWebView2EnvironmentWithDetails` poderá falhar.  Você pode copiar os dados do diretório de dados do usuário antigo para o novo diretório.  

## 0.8.230  

[Pacote NuGet][WebView2NuGetGallery0.8.230] | versão mínima do Microsoft Edge 77.0.230.0.  

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

* `Stop`API adicionada para parar toda a navegação e buscas de recursos pendentes \ ([\ #28][MicrosoftEdgeWebViewFeedbackIssue28]\).  
* Arquivo. tlb adicionado ao pacote NuGet \ ([\ #22][MicrosoftEdgeWebViewFeedbackIssue22]\).  
* Projetos .NET adicionados à lista de instalador no pacote NuGet \ ([\ #32][MicrosoftEdgeWebViewFeedbackIssue32]\).  

## 0.8.190  

[Pacote NuGet][WebView2NuGetGallery0.8.190] | versão mínima do Microsoft Edge 77.0.190.0.  

**Compile novamente o aplicativo após atualizar o pacote NuGet.**

* Adicionado `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` para controlar se os usuários podem abrir o devtools \ ([\ #16][MicrosoftEdgeWebViewFeedbackIssue16]\).  
* Adicionado `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` para controlar se a barra de status for exibida \ ([\ #19][MicrosoftEdgeWebViewFeedbackIssue19]\).  
* Adicionado `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` para voltar e avançar por meio do histórico de navegação.  
* Tipos de cabeçalho http ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` ) adicionados para exibição e modificação de cabeçalhos HTTP no WebView.  
* Suporte adicional para WebView de 32 bits em computadores de 64 bits \ ([\ #13][MicrosoftEdgeWebViewFeedbackIssue13]\).  
* Adicionado webidl ao SDK \ ([\ #14][MicrosoftEdgeWebViewFeedbackIssue14]\).  
* Biblioteca adicionada para dar suporte a objetos de ID de interface IID\_\ * \ ([\ #12][MicrosoftEdgeWebViewFeedbackIssue12]\).  
* Adicionar caminho de inclusão, vinculação e cópia automática de arquivos DLL ao arquivo de destino do NuGet no SDK.  
* Habilitada para solicitação `window.open` em script.  

## 0.8.149  

[Pacote NuGet][WebView2NuGetGallery0.8.149] | versão mínima do Microsoft Edge 76.0.149.0.  

Lançamento inicial do desenvolvedor preview.  

<!-- image links -->

<!-- Links -->
[MicrosoftEdgeWebViewFeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 12"  
[MicrosoftEdgeWebViewFeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 13"  
[MicrosoftEdgeWebViewFeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repositório de comentários para o MicrosoftEdge/WebViewFeedback do problema 14"  
[MicrosoftEdgeWebViewFeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repositório de comentários para o MicrosoftEdge/WebViewFeedback Issue 16"  
[MicrosoftEdgeWebViewFeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 18"  
[MicrosoftEdgeWebViewFeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 19"  
[MicrosoftEdgeWebViewFeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repositório de comentários para o MicrosoftEdge/WebViewFeedback Issue 22"  
[MicrosoftEdgeWebViewFeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 27"  
[MicrosoftEdgeWebViewFeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 28"  
[MicrosoftEdgeWebViewFeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 32"  

[WebView2NuGetGallery]: https://aka.ms/webviewnuget "Galeria do NuGet | Microsoft. Web. WebView2"  
[WebView2NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[WebView2NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[WebView2NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[WebView2NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[WebView2NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[WebView2NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[WebView2NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.9.430"
[WebView2NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.9.488"
[WebView2NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galeria do NuGet | Pré-lançamento do Microsoft. Web. WebView2 v 0.9.515"

[WebViewsGlobalsCreateWebView2EnvironmentWithDetails]: reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "WebView global-função CreateWebView2EnvironmentWithDetails"  
