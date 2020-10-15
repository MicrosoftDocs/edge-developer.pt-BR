---
description: Notas de versão do SDK do Microsoft Edge WebView2
title: Notas de versão do Microsoft Edge WebView2 para Win32, WPF e WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 67380670d2eb499c182d0cc2b53d6d3938c171f1
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119084"
---
# Notas de versão do SDK do WebView2  

A equipe do WebView2 está fornecendo atualizações para o [SDK do WebView2][NuGetGallery] em uma cadência de seis semanas.  Revise o conteúdo a seguir para obter informações atualizadas sobre anúncios de produtos, inclusões e modificações na superfície da API e alterações significativas.  

> [!NOTE]
> Compile novamente o aplicativo após atualizar o pacote NuGet.  

> [!IMPORTANT]
> Embora o WebView2 seja uma visualização, as APIs do .NET estão no `prerelease package` .  

## 0.9.628-pré-lançamento  

Data do lançamento: 10 de setembro de 2020  

[Pacote NuGet][NuGetGallery0.9.628-prerelease] \ | versão mínima do Microsoft Edge 87.0.628.0.  

> [!IMPORTANT]
> **Lançamento**: Este pré-lançamento continua a lançar com base na ramificação do Microsoft Edge 87.  No futuro, a versão do SDK de pré-lançamento corresponde à compilação do Microsoft Edge Canárias e a versão normal está sincronizada com o Microsoft Edge estável.  

#### Geral  

*   > [!IMPORTANT]
    > **Lançamento**: as APIs de hospedagem Visual estão agora em visualização.  O WebView2 usa hospedagem Visual para ser executado juntamente com elementos visuais WinComp/DComp, em oposição a HWNDs.  As interfaces estão em experimental.  Para obter mais informações, acesse [ICoreWebView2ExperimentalEnvironment][ReferenceWin3209622Icorewebview2experimentalenvironment].  

#### .NET  

*   Os binários do .NET agora são [altamente nomeados][DotnetStandardAssemblyStrongNamed].  \ ([\ #181][GithubMicrosoftedgeWebviewfeedbackIssue181]\).  
*   Destino do NuGet atualizado para incluir `WebViewLoader2.dll` .  \ ([\ #228][GithubMicrosoftedgeWebviewfeedbackIssue228]\) e \ ([\ #183][GithubMicrosoftedgeWebviewfeedbackIssue183]\).  
*   Atualizado `WebResourceRequested` para expor APIs [HttpRequestHeaders][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2httprequestheaders] e [HttpResponseHeaders][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2httpresponseheaders] no .net.  \ ([\ #131][GithubMicrosoftedgeWebviewfeedbackIssue131]\).  

## 0.9.622.11  

Data do lançamento: 10 de setembro de 2020  

[Pacote NuGet][NuGetGallery0.9.622.11] \ | WebView2, versão mínima de tempo de execução do 86.0.622.11.  

#### Geral  

*   > [!IMPORTANT]
    > **Lançamento**: este SDK é a versão RC para WebView2 Win32 C/C++ ga.  A versão GA deve usar a mesma interface e funcionalidade de API.  

*   Políticas desconectadas do [navegador][DeployedgeMicrosoftEdgePolicies].  
*   Adicionada a propriedade [AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin3209622Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount] em WebView2 opções de ambiente para habilitar o acesso condicional para WebView.  
*   Atualizado `ICoreWebView2NewWindowRequestedEventArgs` para incluir a propriedade [WindowFeatures][ReferenceWin3209622Icorewebview2newwindowrequestedeventargsGetWindowfeatures] e o [ICoreWebView2WindowFeatures][ReferenceWin3209622Icorewebview2windowfeatures]associado.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Atualizado `System.Windows.Rect`  para usar `System.Drawing.Rectangle` em vez de `System.Windows.Rect` \ ([\ #235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Evento NewWindowRequested atualizado para manipular a `window.open()` solicitação sem parâmetros.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][ReferenceWin3209622Icorewebview2environmentoptionsPutAdditionalbrowserarguments] Set using `ICoreWebView2EnvironmentOptions` não é substituído por variável de ambiente ou valor do registro.  Para obter mais informações, acesse [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209622IdlCreatecorewebview2environmentwithoptions].  

## 0.9.579  

Data do lançamento: 20 de julho de 2020  

[Pacote NuGet][NuGetGallery0.9.579] \ | versão mínima do Microsoft Edge 86.0.579.0.  

#### Geral  

*   > [!IMPORTANT]
    > **Lançamento**: o tempo de execução do WebView2 e o instalador do são lançados para visualização.  Para obter mais informações, navegue até [distribuição de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview].  
*   > [!IMPORTANT]
    > **Lançamento**: as seguintes versões do SDK do WebView2 não têm mais suporte após o próximo lançamento do SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > As versões do SDK do WebView2 também são marcadas preteridas em nuget.org.  O WebView2 recomenda manter-se atualizado com a versão mais recente do WebView2.  

*   Melhorias no thread de trabalho do WebView.  \ ([\ #318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Bloqueador de pop-up desabilitado no WebView.  Para obter mais informações, navegue até a propriedade [IsUserInitiated][ReferenceWin3209538Icorewebview2newwindowrequestedeventargsGetIsuserinitiated] no `NewWindowRequested` evento.  
*   Verificado se o evento de início da navegação do WebView foi acionado `about:blank` .  Agora, `NavigationStarting` os eventos são acionados para toda a navegação, mas cancelamentos para `about:blank` ou iframe srcdoc não têm suporte e são ignorados.  
*   `edge:// URI`Esquema bloqueado no WebView.  
*   Adicionada a propriedade [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin3209538Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled] experimental nas opções de ambiente WebView2 para habilitar o acesso condicional para WebView.  
*   Adicionado um evento [WebResourceResponseReceived][ReferenceWin3209538Icorewebview2experimentalAddWebresourceresponsereceived] experimental que é acionado depois que a WebView recebeu e processou a resposta para uma solicitação WebResource.  Os cabeçalhos de autenticação, se houver, serão incluídos no objeto Response.  

#### .NET  

*   Tratamento aprimorado do foco do WPF.  \ ([\ #185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   `ZoomFactor`Propriedade adicionada ao controlador de Webview2 do WPF.  

## 0.9.538  

[Pacote NuGet][NuGetGallery0.9.538] \ | versão mínima do Microsoft Edge 85.0.538.0.  

#### Geral  

*   Descartando o suporte para o SDK da versão WebView2 do [0.8.149](#08149).  O WebView2 recomenda manter-se atualizado com a versão mais recente do WebView2.  
*   Política de grupo atualizada para conta quando o caminho do perfil do navegador Microsoft Edge é modificado \ ([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  

#### Win32 C/C++  

*   Adicionou [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures], que é acionado quando `window.open()` é executado e associado a [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin3209538Icorewebview2experimentalwindowfeatures] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Alteração significativa**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] é preterido e substituído por [CreateCoreWebView2EnvironmentWithOptions] [[ReferenceWin3209538IdlCreatecorewebview2environmentwithoptions].  
*   > [!IMPORTANT]
    > **Alteração de quebra**: para garantir que a API WebView2 se alinhe com as convenções de nomenclatura da API do Windows, a equipe da WebView atualizou os nomes dos itens a seguir.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed] agora é [AreHostObjectsAllowed][ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed].  
*   [AddHostObjectToScript][ReferenceWin3209538Icorewebview2Addhostobjecttoscript] atualizado para garantir que os marcadores originais do serializador do objeto host sejam definidos como objetos proxy e serializados como um objeto host quando passados como um parâmetro no retorno de chamada do JavaScript \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  

#### .NET (pré-lançamento do 0.9.538)  

*   Exemplos de WinForms e WebView2APIs liberados do WPF, que são guias abrangentes do SDK do WebView2.  Para obter mais informações, navegue até o [repositório de exemplos][GithubMicrosoftedgeWebview2samplesMain].  
*   Suporte adicional para hospedagem visual e recursos de janela [APIs experimentais][ConceptsVersioningExperimentalApis].  
*   > [!IMPORTANT]
    > **Alteração quebrada**: os seguintes adiamentos agora implementam IDisposable:  [ScriptDialogOpening][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]e [PermissionRequested][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   [GetAvailableBrowserVersionString][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] e [CompareBrowserVersions][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] adicionados como estáticos [CoreWebView2Environment][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environment] .  

## 0.9.515-pré-lançamento  

[Pacote NuGet][NuGetGallery0.9.515-prerelease] \ | versão mínima do Microsoft Edge 84.0.515.0.  

*   > [!IMPORTANT]
    > **Lançamento**: o WebView2 agora oferece suporte a formulários do Windows e WPF no .NET Framework 4.6.2 ou posterior e .net Core 3,0 ou posterior no **pacote de pré-lançamento**.  
*   Para obter mais informações sobre como criar aplicativos WPF e a [referência do WPF][ReferenceWpfReference] WebView2 para APIs específicas do WPF, navegue até o guia de introdução ao [WPF][GettingstartedWpf].  
*   Para obter mais informações sobre como criar aplicativos do Windows Forms e a referência WebView2 do [Windows Forms][ReferenceWinformsReference] para APIs específicas do Windows Forms, acesse o [Guia de introdução do Windows Forms][GettingstartedWinforms].  
*   Para obter mais informações sobre as APIs CoreWebView2, navegue até [referência .net][ReferenceDotnetReference].  
*   > [!CAUTION]
    > **Problemas conhecidos**: a equipe da WebView está ciente de alguns problemas na pré-lançamento que estão sendo resolvidos em lançamentos futuros.  
    > *   **Reconhecimento de DPI**: o WEBVIEW2 para WPF não reconhece dpi no momento.  Ao inicializar o WebView2 em monitores High DPI, há um problema conhecido em que o WebView em primeiro inicializa como uma fração da janela até que a janela seja redimensionada.  
    > *   **WPF Designer**: o designer do WPF não tem suporte no momento.  Adicione o controle WebView2 ao seu aplicativo modificando diretamente o XAML apropriado em um editor de texto.  

## 0.9.488  

[Pacote NuGet][NuGetGallery0.9.488] \ | versão mínima do Microsoft Edge 84.0.488.0.  

*   > [!IMPORTANT]
    > **Lançamento**: começando com o próximo Microsoft Edge versão 83, a WebView verde não direciona mais o canal de navegador estável.  Em vez disso, ele se destina a outro conjunto de binários, com a marca de [tempo de execução WebView2][ConceptsDistributionEvergreenMode], que você pode encadear, instalar por meio de um instalador que está desenvolvendo a equipe do WebView.  Para obter mais informações, navegue até [app-Distribution][ConceptsDistribution].  
*   > [!IMPORTANT]
    > **Lançamento**: avançando, a equipe da WebView libera dois pacotes: um pacote de pré-lançamento com APIs experimentais \ (para experimentar \) e um pacote de lançamento estável com APIs estáveis \ (para sua confiança \).  Para saber mais sobre as diferenças, navegue até [noções básicas sobre versões do navegador e WebView2][ConceptsVersioning].  
*   > [!IMPORTANT]
    > **Alteração significativa**: para garantir que a API WebView2 se alinhe com as convenções de nomenclatura da API do Windows, a equipe da WebView atualizou os nomes das interfaces a seguir.  
    > *   `CORE_WEBVIEW2_*` Agora é o prefixo `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo] agora é [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo] agora é [get_BrowserVersionString][ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring].  
    > *   [Addremoteobject][ReferenceWin3209430Icorewebview2Addremoteobject] agora é [AddHostObjectToScript][ReferenceWin3209488Icorewebview2Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][ReferenceWin3209430Icorewebview2Removeremoteobject] agora é [RemoveHostObjectFromScript][ReferenceWin3209488Icorewebview2Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` Agora está `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Alteração de quebra**: os `AddRemoteObject` métodos de proxy do js também são renomeados.  
    > *   `getLocal` Agora está `getLocalProperty` .  
    > *   `setLocal` Agora está `setLocalProperty` .  
    > *   `getRemote` Agora está `getHostProperty` .  
    > *   `setRemote` Agora está `setHostProperty` .  
    > *   `applyRemote` Agora está `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Alteração de quebra**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] é preterida e substituída por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions].  
*   Evento [FrameNavigationCompleted][ReferenceWin3209488Icorewebview2AddFramenavigationcompleted] adicionado.  Agora, quando um iframe concluir a navegação, um evento é acionado e retorna o sucesso da navegação e da ID de navegação.  
*   Adicionada a interface [ICoreWebView2EnvironmentOptions][ReferenceWin3209488Icorewebview2environmentoptions] , que pode ser usada para determinar a versão do tempo de execução do WebView2 para a qual o aplicativo se destina.  
*   Adicionada a configuração [IsBuiltInErrorPageEnabled][ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled] .  Agora, você pode optar por habilitar ou desabilitar a página de erro interna para falha de navegação e falha no processo de renderização.  
*   Injeção de objeto remoto atualizada para dar suporte a implementações do .NET IDispatch \ ([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Evento [NewWindowRequested][ReferenceWin3209488Icorewebview2AddNewwindowrequested] atualizado para manipular solicitações de menus de contexto \ ([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Lançamento do primeiro pacote de pré-lançamento de WebView2 separado onde você pode acessar APIs de hospedagem Visual.  A equipe WebView atualizou o [APISample][GithubMicrosoftedgeWebview2samplesMain] para incluir as novas APIs experimentais.  
    *   Adicionada a interface [ICoreWebView2ExperimentalCompositionController][ReferenceWin3209488Icorewebview2experimentalcompositioncontroller] para se conectar a uma árvore de composição e fornecer a entrada para o WebView.  
    *   Adicionado [ICoreWebView2ExperimentalPointerInfo][ReferenceWin3209488Icorewebview2experimentalpointerinfo], que contém todas as informações de a `POINTER_INFO` .  Esse objeto é passado para SendPointerInput para injetar a entrada do ponteiro no WebView.  
    *   Adicionado [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler], que informa ao aplicativo quando o cursor do mouse sobre a WebView deve ser alterado.  Quando o mouse está sobre uma caixa de texto no WebView, o cursor muda da seta para o seletor.  A `cursor` propriedade no `CompositionController` aplicativo informa ao aplicativo qual o cursor do mouse deve estar no momento para o WebView.  

## 0.9.430  

[Pacote NuGet][NuGetGallery0.9.430] \ | versão mínima do Microsoft Edge 82.0.430.0.  

O SDK do WebView2 é a versão Win32 Win32 beta oficial, que incorpora várias solicitações de recursos de comentários.  A equipe da WebView tenta limitar o número de lançamentos com alterações quebradas, mas como a disponibilidade geral é abordada, a versão beta é usada para incorporar várias alterações significativas em uma única vez.  

*   > [!IMPORTANT]
    > **Alteração de quebra**: como a versão final se aproxima da equipe da WebView, renomeou o prefixo *IWebView2WebView*   como *ICOREWEBVIEW2*   para garantir que a API WebView2 se alinhe com a Convenção de nomenclatura da API do Windows.  Além disso, para aproveitar o SDK do WebView2 de estruturas de interface do usuário, a equipe da WebView separada `ICoreWebView2` em [ICoreWebView2][ReferenceWin3209430Icorewebview2] e [ICoreWebView2Host][ReferenceWin3209430Icorewebview2host].  `ICoreWebView2Host` suporta o redimensionamento, a exibição e a ocultação, o foco e outras funcionalidades relacionadas à janela e composição.  ICoreWebView2 dá suporte a todas as outras funcionalidades do WebView2.  Para saber mais sobre como incorporar as alterações, navegue até a [solicitação pull][GithubMicrosoftedgeWebview2samplesPr17] WebView2 no projeto WebView2 [APISample][GithubMicrosoftedgeWebview2samplesMain] .  
*   > [!IMPORTANT]
    > **Alteração de quebra**: divida o [DocumentStateChanged][ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged] em três componentes:  [SourceChanged][ReferenceWin3209430Icorewebview2AddSourcechanged], [ContentLoading][ReferenceWin3209430Icorewebview2AddContentloading]e [historychanged][ReferenceWin3209430Icorewebview2AddHistorychanged].  Agora, quando a URL de origem muda o `SourceChanged` evento é acionado.  Quando o estado do histórico é alterado, o `HistoryChanged` evento é acionado.  O `ContentLoading` evento é acionado antes do script inicial quando um novo documento está sendo carregado.  
*   Suporte adicional para a arquitetura ARM64.  
*   Adicionado o suporte do painel de entrada do o \ (SIP \) para dispositivos com tela sensível ao toque.  
*   Suporte adicional para Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 e Windows Server 2016.  
*   Adicionado [NotifyParentWindowPositionChanged][ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged] que permite que a barra de status siga a janela no modo de janela.  A alteração também deve ser implementada no modo sem janela para que os recursos de acessibilidade funcionem.  
*   Adicionada a configuração [AreRemoteObjectsAllowed][ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed] para controlar globalmente se uma página pode ser acessada por qualquer objeto remoto.  Por padrão, `AreRemoteObjectsAllowed` está habilitado, o que significa que os objetos remotos adicionados por [addremoteobject][ReferenceWin3209430Icorewebview2Addremoteobject] podem ser acessados da página.  Quando `AreRemoteObjectsAllowed` está desabilitado, os objetos não podem ser acessados da página.  As alterações são aplicadas no próximo evento de navegação.  
*   Adicionada a configuração [IsZoomControlEnabled][ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled] para impedir que os usuários afetem o zoom do WebView usando `ctrl` + `+` e `ctrl` + `-` \ (ou `ctrl` + roda do mouse \).  O zoom ainda poderá ser definido usando [put_ZoomFactor][ReferenceWin3209430Icorewebview2hostPutZoomfactor] quando a configuração estiver desabilitada.  
*   ZoomFactor alterado para aplicar somente ao WebView atual.  As alterações de zoom no WebView atual não afetam outros webviews que você navegou para o mesmo site de origem.  Para obter mais informações, navegue até [get_ZoomFactor][ReferenceWin3209430Icorewebview2hostGetZoomfactor].  
*   Interface de usuário ZoomView HID para WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   [SetBoundsAndZoomFactor][ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor]adicionado.  Agora, você pode definir o fator de zoom e os limites de um WebView ao mesmo tempo.  
*   Evento [WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] adicionado.  Para obter mais informações, navegue até [add_WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] \ ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Foi adicionado suporte para o `beforeunload` tipo de caixa de diálogo para eventos de caixa de diálogo JavaScript e adicionado [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind] entrada de enumeração.  
*   Adicionados [Getheaders][ReferenceWin3209430Icorewebview2httprequestheadersGetheaders] a HttpRequestHeaders, [GetHeader][ReferenceWin3209430Icorewebview2httpresponseheadersGetheader] para HttpResponseHeaders, e a propriedade [get_HasCurrentHeader][ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader] para HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Alteração significativa**: `DevToolsProtocolEventReceived` comportamento modificado.  Agora, você pode criar um [DevToolsProtocolEventReceiver][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver] para um evento de protocolo de devtools específico e assinar/cancelar a assinatura para esse evento usando [add_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived].
*   > [!IMPORTANT]
    > **Alteração de quebra**: alterou a propriedade WebMessageReceivedEventArgs ' [get_WebMessageAsString][ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring] para um método [TryGetWebMessageAsString][ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring] .  
*   > [!IMPORTANT]
    > **Alteração de quebra**: `AcceleratorKeyPressedEventArgs` método [Handle][ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle] alterado para uma propriedade [get_Handled][ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled] .  

## 0.8.355

[Pacote NuGet][NuGetGallery0.8.355] \ | versão mínima do Microsoft Edge 80.0.355.0.

*   Exemplo de WebView2API lançada, um guia abrangente do SDK do WebView2.  Para obter mais informações, acesse [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Suporte do IME adicionado para todos os idiomas além do inglês \ ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Atualizou a superfície de API do `WebResourceRequested` evento em resposta a relatórios de erros.  A especificação simultânea de um filtro e um evento de criação já foi preterido.  Para criar um evento de recurso da Web solicitado, use [add_WebResourceRequested][ReferenceWin3208190Iwebview2webview5AddWebresourcerequested] para adicionar o evento e [AddWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter] para adicionar um filtro.  [RemoveWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter] remove o filtro \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Alteração significativa**: comportamento de tela inteira modificada.  [IsFullScreenAllowed][ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]preterido.  Agora, por padrão, se um elemento em uma WebView \ (como um vídeo \) estiver definido como tela inteira, ele preenche os limites do WebView.  Use o evento [ContainsFullScreenElementChanged][ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler] e [get_ContainsFullScreenElement][ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement] para especificar como o aplicativo deve redimensionar o WebView se um elemento quiser entrar em modo de tela inteira.  

## 0.8.314  

[Pacote NuGet][NuGetGallery0.8.314] \ | versão mínima do Microsoft Edge 80.0.314.0.  

*   Suporte adicional para Windows 7, Windows 8 e Windows 8,1.  
*   Adicionado o suporte de depuração de código do Visual Studio e do Visual Studio para WebView2.  Agora, depure o script no WebView2 diretamente do IDE.  Para obter mais informações, navegue até [como depurar ao desenvolver com controles WebView2][HowtoDebug].  
*   Adicionado `Native Object Injection` , que permite que o script em execução no WebView2 acesse um objeto IDispatch do componente Win32 do aplicativo e acesse as propriedades do objeto IDispatch.  Para obter mais informações, navegue até [Addremoteobject][ReferenceWin3208190Iwebview2webview4Addremoteobject] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   `AcceleratorKeyPressed`Evento adicionado.  Para obter mais informações, navegue até [add_AcceleratorKeyPressed][ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Desabilitado `Context Menus` .  Para obter mais informações, navegue até [put_AreDefaultContextMenusEnabled][ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Atualizado `DPI Awareness` .  Agora, o reconhecimento de DPI do WebView é o mesmo que o reconhecimento de DPI do aplicativo host.  
    
    > [!NOTE]
    > Se outro aplicativo híbrido for iniciado com um reconhecimento de DPI diferente do que o WebView original, o novo WebView não será iniciado se o diretório de dados do usuário for o mesmo \ ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Atualizado `Notification Change Behavior` para que o WebView2 rejeite automaticamente solicitações de permissão de notificação solicitadas pelo conteúdo da Web hospedado no WebView.  

## 0.8.270  

[Pacote NuGet][NuGetGallery0.8.270] \ | versão mínima do Microsoft Edge 78.0.270.0.  

*   Adicionado `DocumentTitleChanged` evento para indicar a mudança de título do documento \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   `GetWebView2BrowserVersionInfo`API adicionada \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   `NewWindowRequested`Evento adicionado.  
*   `CreateWebView2EnvironmentWithDetails`Função updated a ser removida `releaseChannelPreference` .  Para obter mais informações sobre a `CreateWebView2EnvironmentWithDetails` função, navegue até [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails].  Ainda há suporte para a substituição da variável de ambiente e do registro.  A preferência de canal padrão é usada, a menos que seja substituída.  
    Durante a pesquisa de canais, a equipe da WebView ignora qualquer versão de canal mais antiga que não seja compatível com o SDK do WebView2.  
    A equipe da WebView seleciona o canal mais estável para garantir os comportamentos mais consistentes para o usuário final.  Ao testar com as versões mais recentes do Canárias, você deve criar um script para definir a `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` variável de ambiente `1` antes de iniciar o aplicativo.  
*   Atualização da `CreateWebView2EnvironmentWithDetails` função com lógica para selecionar `userDataFolder` quando não especificado.  Para obter mais informações sobre a `CreateWebView2EnvironmentWithDetails` função, navegue até [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails].  Se você usou anteriormente o `userDataFolder` local padrão, ao alternar para o novo SDK, o padrão `userDataFolder` será Reset \ (definido como um novo local no diretório de código do host \) e seu estado também será redefinido.  
    Se o processo de host não tiver permissão para gravar no diretório especificado, a `CreateWebView2EnvironmentWithDetails` função poderá falhar.  Você pode copiar os dados do diretório de dados do usuário antigo para o novo diretório.  

## 0.8.230  

[Pacote NuGet][NuGetGallery0.8.230] \ | versão mínima do Microsoft Edge 77.0.230.0.  

*   `Stop`API adicionada para parar toda a navegação e buscas de recursos pendentes \ ([\ #28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   `.tlb`Arquivo adicionado ao pacote NuGet \ ([\ #22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Projetos .NET adicionados à lista de instalador no pacote NuGet \ ([\ #32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  

## 0.8.190  

[Pacote NuGet][NuGetGallery0.8.190] \ | versão mínima do Microsoft Edge 77.0.190.0.  

*   Adicionado `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` para controlar se os usuários podem abrir o devtools \ ([\ #16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Adicionado `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` para controlar se a barra de status for exibida \ ([\ #19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Adicionado `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` para voltar e avançar por meio do histórico de navegação.  
*   Adicionados tipos de cabeçalho HTTP \ ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) para exibir e modificar cabeçalhos HTTP no WebView.  
*   Suporte adicional para WebView de 32 bits em computadores de 64 bits \ ([\ #13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Adicionado webidl ao SDK \ ([\ #14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Biblioteca adicionada para dar suporte a `IID\_\*` objetos de ID de interface \ ([\ #12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Adicionar caminho de inclusão, vinculação e cópia automática de arquivos DLL ao arquivo NuGet `TARGET` no SDK.  
*   Habilitada para solicitação `window.open()` em script.  

## 0.8.149  

[Pacote NuGet][NuGetGallery0.8.149] \ | versão mínima do Microsoft Edge 76.0.149.0.  

Lançamento inicial do desenvolvedor preview.  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Modo de distribuição em verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./concepts/distribution.md#understanding-the-webview2-runtime "Compreenda o tempo de execução do WebView2 e o instalador (visualização)-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ConceptsVersioning]: ./concepts/versioning.md "Noções básicas sobre versões do navegador e WebView2 | Documentos da Microsoft"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "APIs experimentais-noções básicas sobre versões do navegador e WebView2 | Documentos da Microsoft"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Introdução ao WebView2 em aplicativos do Windows Forms | Documentos da Microsoft"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Introdução ao WebView2 no WPF | Documentos da Microsoft"  
[HowtoDebug]: ./howto/debug.md "Como depurar ao desenvolver com controles WebView2 | Documentos da Microsoft"  

[ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Identificador da interface de IWebView2AcceleratorKeyPressedEventArgs | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interface IWebView2ContainsFullScreenElementChangedEventHandler | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled-interface IWebView2Settings2 | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated-interface IWebView2Settings | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString-interface IWebView2WebMessageReceivedEventArgs | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed-interface IWebView2WebView4 | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged-interface IWebView2WebView | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webview4Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "Addremoteobject-interface IWebView2WebView4 | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webview5AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested-interface IWebView2WebView5 | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter-interface IWebView2WebView5 | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement-interface IWebView2WebView5 | Documentos da Microsoft"  
[ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter-interface IWebView2WebView5 | Documentos da Microsoft"  
[ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-globais | Documentos da Microsoft"  

[ReferenceWin3209430Icorewebview2]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled-interface ICoreWebView2AcceleratorKeyPressedEventArgs | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "Addremoteobject-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived-interface ICoreWebView2DevToolsProtocolEventReceiver | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived-interface ICoreWebView2DevToolsProtocolEventReceiver | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo-interface ICoreWebView2Environment | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2host]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2Host | Documentos da Microsoft"  
[ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-globais | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2hostGetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor-interface ICoreWebView2Host | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged-interface ICoreWebView2Host | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2hostPutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor-interface ICoreWebView2Host | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor-interface ICoreWebView2Host | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader-interface ICoreWebView2HttpHeadersCollectionIterator | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2httprequestheadersGetheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "Getheaders-interface ICoreWebView2HttpRequestHeaders | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2httpresponseheadersGetheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader-interface ICoreWebView2HttpResponseHeaders | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-interface ICoreWebView2Settings | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled-interface ICoreWebView2Settings | Documentos da Microsoft"  
[ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString-interface ICoreWebView2WebMessageReceivedEventArgs | Documentos da Microsoft"  

[ReferenceWin3209488Icorewebview2AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2environmentoptions]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2EnvironmentOptions | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalcompositioncontroller]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2ExperimentalCursorChangedEventHandler | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalpointerinfo]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2ExperimentalPointerInfo | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-interface ICoreWebView2Settings | Documentos da Microsoft"  
[ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Documentos da Microsoft"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-globais | Documentos da Microsoft"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-globais | Documentos da Microsoft"  
[ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-globais | Documentos da Microsoft"  

[ReferenceDotnetReference]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft. Web. WebView2. Core | Documentos da Microsoft"  
[ReferenceWpfReference]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft. Web. WebView2. WPF | Documentos da Microsoft"  
[ReferenceWinformsReference]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft. Web. WebView2. WinForms | Documentos da Microsoft"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Classe CoreWebView2Environment (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Método CoreWebView2Environment. CompareBrowserVersions (cadeia de caracteres, Cadeia de caracteres) (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Método CoreWebView2Environment. GetAvailableBrowserVersionString (cadeia de caracteres) (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Evento CoreWebView2. NewWindowRequested (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Evento CoreWebView2. PermissionRequested (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Evento CoreWebView2. ScriptDialogOpening (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Evento CoreWebView2. WebResourceRequested (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Classe CoreWebView2HttpRequestHeaders (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  
[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Classe CoreWebView2HttpResponseHeaders (Microsoft. Web. WebView2. Core) | Documentos da Microsoft"  

[ReferenceWin3209538Icorewebview2Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript-interface ICoreWebView2 | Documentos da Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived-interface ICoreWebView2Experimental | Documentos da Microsoft"  
[ReferenceWin3209538Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled-interface ICoreWebView2ExperimentalEnvironmentOptions | Documentos da Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_windowfeatures "get_WindowFeatures-interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Documentos da Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalwindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538&preserve-view=true "interface ICoreWebView2ExperimentalWindowFeatures | Documentos da Microsoft"  
[ReferenceWin3209538Icorewebview2newwindowrequestedeventargsGetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "interface do get_IsUserInitiated ICoreWebView2NewWindowRequestedEventArgs | Documentos da Microsoft"  
[ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed-interface ICoreWebView2Settings | Documentos da Microsoft"  
[ReferenceWin3209538IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-globais | Documentos da Microsoft"  

[ReferenceWin3209622Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount-interface ICoreWebView2EnvironmentOptions | Documentos da Microsoft"  
[ReferenceWin3209622Icorewebview2environmentoptionsPutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments-interface ICoreWebView2EnvironmentOptions | Documentos da Microsoft"  
[ReferenceWin3209622Icorewebview2experimentalenvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.622&preserve-view=true "interface ICoreWebView2ExperimentalEnvironment | Documentos da Microsoft"  
[ReferenceWin3209622Icorewebview2newwindowrequestedeventargsGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures-interface ICoreWebView2NewWindowRequestedEventArgs | Documentos da Microsoft"  
[ReferenceWin3209622Icorewebview2windowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interface ICoreWebView2WindowFeatures | Documentos da Microsoft"  
[ReferenceWin3209622IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-globais | Microsoft Edge"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge-políticas | Documentos da Microsoft"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblies de nome forte | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repositório de comentários para o MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repositório de comentários para o MicrosoftEdge/WebViewFeedback do problema 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repositório de comentários para o MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repositório de comentários para o MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 108"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 119"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 131"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 185"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 235"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Repositório de comentários para o problema do MicrosoftEdge/WebViewFeedback 318"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Mover projeto para usar o SDK do WebView2 mais recente 0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemplo de API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Galeria do NuGet | Microsoft. Web. WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galeria do NuGet | Pré-lançamento do Microsoft. Web. WebView2 v 0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Galeria do NuGet | Microsoft. Web. WebView2 v 0.9.622.11"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Galeria do NuGet | Pré-lançamento do Microsoft. Web. WebView2 v 0.9.628"  
