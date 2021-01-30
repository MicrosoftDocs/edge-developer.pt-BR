---
description: Notas de versão do SDK do Microsoft Edge WebView2
title: Notas de versão do Microsoft Edge WebView2 para Win32, WPF e WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, controle de navegador, html de borda
ms.openlocfilehash: ebb8b0afc4729233a069ba9979537e5a78fcc941
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306259"
---
# Notas de versão do SDK webView2  

A equipe WebView2 atualiza o [SDK webView2][NuGetGallery] em uma cadência de seis semanas.  Revise o conteúdo a seguir para obter informações atualizadas sobre anúncios de produtos, adições, modificações e alterações significativas nas APIs.  

> [!NOTE]
> Certifique-se de compilar seu aplicativo depois de atualizar o pacote NuGet.  A equipe recomenda usar o canal Canary ao desenvolver usando os pacotes de pré-lançamento e o tempo de execução ainda maior ao usar pacotes lançados.  Para obter mais informações, navegue até [Versioning][VersioningDoc].  
 
## 1.0.781-prerelease  

Data do lançamento: 29 de janeiro de 2021  

[Pacote NuGet][NuGetGallery1.0.781-prerelease] \| Microsoft Edge versão 86.0.616.0 ou mais recente  

### Geral  

> [!IMPORTANT]
> O pacote de pré-lançamento WebView2 0.9.430 foi preterido e está sendo removido da próxima versão.  Se o aplicativo WebView usar o pacote, recomendamos atualizar para um pacote mais novo.  

##### Recursos  

*   Adicionado [o método TrySuspend e Resume][ReferenceWin32Icorewebview210781PreReleaseTrySuspendResume] para suspender e retomar WebViews.  
*   Adicionado [o método SetVirtualHostNameToFolderMapping][ReferenceWin32Icorewebview210781PreReleaseSetVirtualHostNameToFolderMapping] que mapeia um nome de host virtual para um caminho de diretório.  
*   Adicionada a [propriedade DefaultBackgroundColor][ReferenceWin32Icorewebview2controllerViewWebview210781PreReleaseDefaultBackgroundColor] para definir a cor e o canal alfa do plano de fundo.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\)  
*   Adicionada a [propriedade UserAgent][ReferenceWin32Icorewebview2experimentalsettings10781PreReleaseGetUserAgent] para obter ou definir o Agente do Usuário. \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue549]\)
*   Substituiu o `CreateCookieWithCookie` método pelo `CopyCookie` método.  
*   Adicionado suporte de hospedagem visual usando a interface [ICoreWebView2CompositionController,][ReferenceWin32Icorewebview2controllerViewWebview210781CompositionController] que é criada usando o novo `CreateCoreWebView2CompositionController` método de `ICoreWebView2Environment3` .  

    
##### Correções de bugs  

*   O recurso De compras do Microsoft Edge no WebView2 foi desligado.  
*   Desligar o menu de contexto no visualizador de PDF quando `AreDefaultContextMenusEnabled` `false` for.  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Correção de um bug `E_NOINTERFACE` que retornava ao consultar `ICoreWebView2` por `ICoreWebView2Experimental` .  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Correção de um bug que permitia a navegação com URIs malformadas `CoreWebView2NavigationStartingEventArgs.Cancel` quando estava definido como `false` .  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Correção de um bug bloqueado `window.print()` em janelas pop-up com manipuladores de eventos anexados a `NewWindowRequested` eventos.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Corrigido um problema de DPI dinâmico ao mover aplicativos entre monitores diferentes.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Aprimorado `HRESULT` o s passado por [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke][ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerInvoke10781].  
    
##### Promoções  

*   As seguintes APIs experimentais agora são promovidas para Estável.  
    *   APIs de hospedagem visual.  
    *   [SetVirtualHostNameToFolderMapping][ReferenceWin32Icorewebview210781PreReleaseSetVirtualHostNameToFolderMapping]  
    *   [TrySuspend e Resume][ReferenceWin32Icorewebview210781PreReleaseTrySuspendResume] 
    *   [DefaultBackgroundColor][ReferenceWin32Icorewebview2controllerViewWebview210781PreReleaseDefaultBackgroundColor]  
    
#### .NET  

##### Correções de bugs  

*   Corrigido um bug que falhava em aplicativos WebView que usam o SDK do WPF.  A falha ocorreu quando as janelas foram fechadas usando a tecla F4.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\)
*   A tela de inicialização do WebView2 agora é transparente, em vez de cinza.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\)
    
## 1.0.705.50  

Data do lançamento: 25 de janeiro de 2021  

[Pacote NuGet][NuGetGallery1.0.705.50] \| WebView2 Runtime versão 86.0.616.0 ou mais recente  

##### Promoções  

*   As seguintes APIs experimentais agora são promovidas para Estável.  
    *   [WebResourceResponseReceived API][WebResourceResponseReceivedAPI]  
    *   [NavigateWithWebResourceRequest API][NavigateWithWebResourceRequestAPI]  
    *   [API de gerenciamento de cookies][CookiemanagementAPI]  
    *   [DOMContentLoaded API][DOMContentLoadedAPI]  
    *   [Propriedade WebView Environment][WebViewEnvironmentproperty]  

## 1.0.721-prerelease  

Data do lançamento: 8 de dezembro de 2020  

[Pacote NuGet][NuGetGallery1.0.721-prerelease] \| Microsoft Edge versão 86.0.616.0 ou mais recente  

#### Geral  

> [!IMPORTANT]
> **Alteração de**quebra: os pacotes de pré-lançamento WebView2 1.0.707 e 0.9.628 foram preterido.  Interrompa o desenvolvimento com esses pacotes.  

###### Recursos  

*   Políticas [de Grupo WebView2 adicionadas.][DeployedgeMicrosoftEdgeWebviewPolicies]  Para obter mais informações sobre as práticas recomendadas, navegue até [políticas de grupo para WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Alteração de**Quebra: preterido o antigo local do Registro.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Adicionado suporte para [Arrastar e Soltar][ReferenceWin32Icorewebview2experimentalcompositioncontroller3] em WebView2.  
*   APIs adicionadas para lidar com o suporte a DPI.  
    *   Adicionada [a propriedade RasterizationScale][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] para alterar a escala de DPI para pop-ups de interface do usuário e conteúdo WebView e [evento RasterizationScaleChanged][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] associado.  
    *   Adicionada [a propriedade ShouldDetectMonitorScaleChanges][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges] para atualizar `RasterizationScale` automaticamente a propriedade, se necessário.  
    *   Adicionada a propriedade [BoundsMode][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode] para especificar que os limites são pixels lógicos e permitir que WebView use para exibição de pixels WebView2 e WebView usar o com o para obter o `RasterizationScale` `RasterizationScale` tamanho `Bounds` físico.  
*   Evento `NewWindowRequested` atualizado para manipular e `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] e [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   As seguintes APIs experimentais agora são promovidas para Estável.  
    *   [WebResourceResponseReceived API][WebResourceResponseReceivedAPI]  
    *   [NavigateWithWebResourceRequest API][NavigateWithWebResourceRequestAPI]  
    *   [API de gerenciamento de cookies][CookiemanagementAPI]  
    *   [DOMContentLoaded API][DOMContentLoadedAPI]  
    *   [Propriedade WebView Environment][WebViewEnvironmentproperty]  
        
#### .NET  

###### Recursos  

*   Ligado o designer WinForms no .NET Core 3.1+ e .NET 5.  
*   Gerenciamento de cookie do .NET aprimorado.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Substituído por `CoreWebView2Ready` [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  

###### Correções de bugs

*   Adicionado [evento AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] para dar suporte a AcceleratorKey pressione em WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Removidos os arquivos desnecessários da saída para pastas WebView2.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   API de objeto host aprimorada.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] e [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## 1.0.664.37  

Data do lançamento: 20 de novembro de 2020  

[Pacote NuGet][NuGetGallery1.0.664.37] \| WebView2 Runtime versão 86.0.616.0 ou mais recente.  

#### Geral  

> [!IMPORTANT]
> **Comunicado**: SDKs .NET WPF/WinForms WebView2 agora estão geralmente disponíveis \(GA\).  A partir desta versão, os SDKs de versão são compatíveis com o encaminhamento.  Para obter mais detalhes, navegue até [a postagem do blog de comunicado GA.][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]  

###### Recursos  

*   O .NET WPF/WinForms WebView2 agora está geralmente disponível \(GA\).  
*   O modo de distribuição fixa \(Traga-seu-próprio\) atingiu GA.  
    
#### .NET  

###### Correções de bugs  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` impede que a nova janela seja aberta \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549]\) e \([\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## 1.0.674-prerelease  

Data do lançamento: 19 de outubro de 2020  

[Pacote NuGet][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime versão 86.0.616.0 ou mais recente.  

#### Geral  

*   Adicionado [o método NavigateWithWebResourceRequest][ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674] para fornecer dados de postagem ou outros headers de solicitação durante a navegação.  
*   Adicionado [o evento DOMContentLoaded][ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674] que é executado quando o documento HTML inicial é carregado e analisado.  
*   A propriedade [Environment][ReferenceWin32Icorewebview2experimentalGetEnvironment10674] foi adicionada a WebView2.  Essa propriedade expõe o ambiente WebView2 onde uma instância de WebView2 foi criada.  
*   ApIs [de gerenciamento de cookie][ReferenceWin32Icorewebview2experimentalGetCookiemanager10674] adicionadas que permitem aos desenvolvedores autenticar a sessão WebView2 ou recuperar cookies do WebView para autenticar outras ferramentas.  A equipe do Webview está planejando fazer melhorias específicas de linguagem ou estrutura.  Para obter mais informações, navegue até Análise [de API: Gerenciamento de Cookies.][GithubMicrosoftedgeWebview2AnnouncementIssue2]  
*   Atualizou o evento [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674] e adicionou [WebResourceResponseView][ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674] e [WebResourceResponseReceivedEventArgs::P opulateResponseContent][ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628] a [WebResourceResponseView::GetContent][ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674].  
*   O [Microsoft Defender Application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] foi desligado no WebView2.  
*   [SystemCursorId adicionado para][ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674] hospedagem visual.  
*   Adicionado bug corrigido para o método de entrada na hospedagem visual.  
*   Removidos incluem `version.lib` requisitos para ao usar a biblioteca estática WebView2.  
    
#### .NET  

*   Classe [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] atualizada para expor a `CoreWebView2Environment` variável.  
*   Implementações alteradas de classes EventArgs personalizadas no namespace para `Microsoft.Web.WebView2.Core` subclasses de [System.EventArgs][DotnetApiSystemEventargs] ou [System.ComponentModel.CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Adicionado suporte para [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] em WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\)
*   ApIs [webResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET adicionadas.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Propriedade WinForms Designer [Source][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] atualizada como padrão ou redefinida como nulo.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Limites de WebView2 atualizados WebView2.Init() para dar suporte a modos DPI menores que 100%.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   [BuildWindowCore e][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] atualizados para aumentar a robustez.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Base atualizada do Carregador do .NET para carregar no bit de processo em vez da arquitetura do sistema operacional.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Renomeado `EdgeNotFoundExpection` para [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## 1.0.622.22  

Data do lançamento: 19 de outubro de 2020  

[Pacote NuGet][NuGetGallery1.0.622.22] \| WebView2 Runtime versão 86.0.616.0 ou mais recente.  

#### Geral  

> [!IMPORTANT]
> **Comunicado**: Win32 C/C++ WebView2 agora está geralmente disponível \(GA\).  A partir desta versão, os SDKs de versão são compatíveis com o encaminhamento.  Para obter mais informações, navegue até [a postagem do blog de comunicado GA.][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]  

*   [Evergreen WebView2 Runtime and installer][Webview2ConceptsDistributionUnderstandRuntimeInstaller] are GA.  Bootstrapper, link downlink para o Bootstrapper e o Instalador Autônomo para o Evergreen WebView2 Runtime estão disponíveis no [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  O código de exemplo para o fluxo de trabalho de instalação também está disponível no [repo WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   [O modo de versão fixa][Webview2ConceptsDistributionFixedVersionMode] está disponível para visualização do desenvolvedor.  
    
## 0.9.622.11  

Data do lançamento: 10 de setembro de 2020  

[Pacote NuGet][NuGetGallery0.9.622.11] \| WebView2 Runtime versão 86.0.616.0 ou mais recente.  

#### Geral  

*   > [!IMPORTANT]
    > **Comunicado**: Este SDK é o Release Candidate for WebView2 Win32 C/C++ GA.  A versão GA deve usar a mesma interface e funcionalidade de API.  
    
*   Políticas de [navegador desconectadas.][DeployedgeMicrosoftEdgePolicies]  
*   Adicionada [a propriedade AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622] nas opções de ambiente WebView2 para ativar o acesso condicional para WebView.  
*   Atualizado `ICoreWebView2NewWindowRequestedEventArgs` para incluir a propriedade [WindowFeatures][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622] e o [ICoreWebView2WindowFeatures associado.][ReferenceWin32Icorewebview2windowfeatures09622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Atualizado `System.Windows.Rect`  para usar em vez de `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Evento NewWindowRequested atualizado para manipular a `window.open()` solicitação sem parâmetros.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments especificados][ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622] por não são substituídos por variáveis de ambiente `ICoreWebView2EnvironmentOptions` ou valores do Registro.  Para obter mais informações, navegue até [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622].  
    
## 0.9.579  

Data do lançamento: 20 de julho de 2020  

[Pacote NuGet][NuGetGallery0.9.579] \| Microsoft Edge versão 86.0.579.0.  

#### Geral  

*   > [!IMPORTANT]
    > **Comunicado**: O Instalador e o Tempo de Execução da Web Evergreen WebView2 são lançados para visualização.  Para obter mais informações, [navegue até Distribuição de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller].  
    
*   > [!IMPORTANT]
    > **Comunicado**: As seguintes versões do SDK WebView2 não são mais suportadas após a próxima versão do SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > As versões do SDK webView2 também são marcadas como preterida nuget.org.  WebView2 recomenda manter-se atualizado com a versão mais recente do WebView2.  
    
*   Melhorias no thread de trabalho do WebView adicionadas.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Desligado o bloqueador de pop-ups no WebView.  Para obter mais informações, navegue até a [propriedade IsUserInitiated][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538] no `NewWindowRequested` evento.  
*   O evento de início de navegação WebView assegurado é executado para `about:blank` .  Agora, os eventos são executados para toda a navegação, mas cancelamentos para ou iframe não `NavigationStarting` `about:blank` são `srcdoc` suportados e ignorados.  
*   Bloqueado alguns `edge://` esquemas de URI no WebView.  
*   Adicionada a propriedade experimental [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538] nas opções de ambiente WebView2 para ativar o acesso condicional para WebView.  
*   Foi adicionado o evento experimental [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538] que é executado depois que o WebView recebe e processa a resposta de uma solicitação WebResource.  Os headers de autenticação, se algum, são incluídos no objeto de resposta.  
    
#### .NET  

*   Tratamento de foco do WPF aprimorado.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Propriedade `ZoomFactor` adicionada no controlador Webview2 do WPF.  
    
## 0.9.538  

[Pacote NuGet][NuGetGallery0.9.538] \| Microsoft Edge versão 85.0.538.0.  

#### Geral  

*   Suporte para o SDK WebView2 versão [0.8.149](#08149).  WebView2 recomenda manter-se atualizado com a versão mais recente do WebView2.  
*   Política de grupo atualizada para levar em conta quando o caminho de perfil do navegador Microsoft Edge é modificado \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
#### Win32 C/C++  

*   Adicionado [ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538], que é a ser executado e associado a `window.open()` [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin32Icorewebview2experimentalwindowfeatures09538] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Alteração de**Quebra : Deprecated [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] e substituído por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538].  
    
*   > [!IMPORTANT]
    > **Alteração de**alteração: para garantir que a API WebView2 se alinhe com as convenções de nomenais da API do Windows, a equipe WebView atualizou os nomes dos seguintes.  
    > 
    > *   [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488] agora [é AreHostObjectsAllowed][ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538].  
    
*   Atualizado [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09538].  Os marcadores do serializador do objeto host original agora estão definidos para os objetos proxy.  Em seguida, os marcadores de serializador de objeto host são serializados de volta como um objeto host quando passados como um parâmetro no retorno de chamada JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
#### .NET (pré-lançamento 0.9.538)  

*   Lançados WinForms e exemplos WPF WebView2API, que são guias abrangentes do SDK WebView2.  Para obter mais informações, navegue [até o Exemplos de Repo][GithubMicrosoftedgeWebview2samplesMain].  
*   Adicionado suporte para apIs experimentais de hospedagem visual e [janela.][ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Alteração de**Alteração: os adiamentos a seguir agora implementam IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]e [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] e [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] foram adicionados como estática [CoreWebView2Environment.][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]  
    
## 0.9.515-prerelease  

[Pacote NuGet][NuGetGallery0.9.515-prerelease] \| Microsoft Edge versão 84.0.515.0.  

*   > [!IMPORTANT]
    > **Comunicado**: WebView2 agora dá suporte a Windows Forms e WPF no .NET Framework 4.6.2 ou posterior e .NET Core 3.0 ou posterior no pacote de **pré-lançamento.**  
    
*   Para obter mais informações sobre como criar aplicativos WPF, navegue até o Guia de Iniciação do [WPF][GettingstartedWpf] e a Referência [WPF][DotnetApiMicrosoftWebWebview2Wpf] WebView2 para APIs específicas do WPF.  
*   Para obter mais informações sobre como criar aplicativos do Windows Forms, navegue até o Guia de Guia de Iniciação do [Windows Forms][GettingstartedWinforms] e a Referência de Formulários do [Windows][DotnetApiMicrosoftWebWebview2Winforms] WebView2 para APIs específicas do Windows Forms.  
*   Para obter mais informações sobre as APIs CoreWebView2, navegue até [.NET Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Problemas conhecidos:** a equipe webview está ciente de alguns problemas no pré-lançamento que estão sendo resolvidos em versões futuras.  
    > 
    > *   **Reconhecimento de DPI**: WebView2 para WPF atualmente não reconhece DPI.  Ao inicializar WebView2 em monitores de DPI alto, há um problema conhecido em que o WebView inicialmente é inicializado como uma fração da janela até que a janela seja relizada.  
    > *   **Designer WPF**: O designer WPF não tem suporte no momento.  Adicione o controle WebView2 em seu aplicativo modificando diretamente o XAML apropriado em um editor de texto.  
    
## 0.9.488  

[Pacote NuGet][NuGetGallery0.9.488] \| Microsoft Edge versão 84.0.488.0.  

*   > [!IMPORTANT]
    > **Comunicado:** a partir da próxima versão do Microsoft Edge 83, o Evergreen WebView não direciona mais o canal do navegador Estável.  Em vez disso, ele tem como alvo outro conjunto de binários, com a marca [Evergreen WebView2 Runtime,][ConceptsDistributionEvergreenMode]que você pode encadear por meio de um instalador que a equipe WebView está desenvolvendo no momento.  Para obter mais informações, navegue até [Distribuição de Aplicativo.][ConceptsDistribution]  
    
*   > [!IMPORTANT]
    > **Comunicado:** seguindo em frente, a equipe WebView lança dois pacotes: um pacote de pré-lançamento com APIs experimentais \(para você experimentar\) e um pacote de versão estável com APIs estáveis \(para sua confiança\).  Para saber mais sobre as diferenças, navegue até [Noções básicas sobre versões do navegador e WebView2][ConceptsVersioning].  
    
*   > [!IMPORTANT]
    > **Alteração de**alteração: para garantir que a API WebView2 se alinhe com as convenções de nomenais da API do Windows, a equipe WebView atualizou os nomes das interfaces a seguir.  
    > 
    > *   `CORE_WEBVIEW2_*` prefixo `COREWEBVIEW2_*` agora.  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430] agora é [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488].  
    > *   [get_BrowserVersionInfo][ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430] agora é [get_BrowserVersionString][ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488].  
    > *   [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] agora [é AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09488].  
    > *   [RemoveRemoteObject][ReferenceWin32Icorewebview2Removeremoteobject09430] agora [é RemoveHostObjectFromScript][ReferenceWin32Icorewebview2Removehostobjectfromscript09488].  
    > *   `chrome.webview.remoteObjects` é agora `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Alteração de**Quebra: os `AddRemoteObject` métodos de proxy JS também são renomeados.  
    > 
    > *   `getLocal` é agora `getLocalProperty` .  
    > *   `setLocal` é agora `setLocalProperty` .  
    > *   `getRemote` é agora `getHostProperty` .  
    > *   `setRemote` é agora `setHostProperty` .  
    > *   `applyRemote` é agora `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Alteração de**Quebra : Deprecated [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] e substituído por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488].  
    
*   Evento [FrameNavigationCompleted][ReferenceWin32Icorewebview2AddFramenavigationcompleted09488] adicionado.  Agora, quando um iframe conclui a navegação, um evento é executado e retorna o sucesso da navegação e da ID de navegação.  
*   Adicionada a interface [ICoreWebView2EnvironmentOptions,][ReferenceWin32Icorewebview2environmentoptions09488] que pode ser usada para determinar a versão do WebView2 Runtime direcionada por seu aplicativo.  
*   A [configuração IsBuiltInErrorPageEnabled][ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488] foi adicionada.  Agora, você pode optar por ativar ou desativar a página da Web de erro interna para falha de navegação e falha no processo de renderização.  
*   Injeção de objeto remoto atualizada para dar suporte a implementações do .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Evento [NewWindowRequested][ReferenceWin32Icorewebview2AddNewwindowrequested09488] atualizado para manipular solicitações de menus de contexto \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Lançado o primeiro pacote de pré-lançamento webView2 separado onde você pode acessar APIs de hospedagem visual.  A equipe do WebView [atualizou a APISample][GithubMicrosoftedgeWebview2samplesMain] para incluir as novas APIs experimentais.  
    
    *   A interface [ICoreWebView2ExperimentalCompositionController][ReferenceWin32Icorewebview2experimentalcompositioncontroller09488] foi adicionada para se conectar a uma árvore de composição e fornecer entrada para o WebView.  
    *   Adicionado [ICoreWebView2ExperimentalPointerInfo][ReferenceWin32Icorewebview2experimentalpointerinfo09488], que contém todas as informações de um `POINTER_INFO` .  Esse objeto é passado para SendPointerInput para injetar entrada de ponteiro no WebView.  
    *   Adicionado [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488], que informa ao aplicativo quando o cursor do mouse sobre o WebView deve ser alterado.  Quando o mouse está sobre uma caixa de texto no WebView, o cursor muda da seta para o seletor.  A propriedade no aplicativo informa ao aplicativo qual deve ser o cursor do `cursor` mouse atualmente para o `CompositionController` WebView.  
    
## 0.9.430  

[Pacote NuGet][NuGetGallery0.9.430] \| Microsoft Edge versão 82.0.430.0.  

O SDK webView2 é a versão beta oficial do Win32 C++, que incorpora várias solicitações de recursos de comentários.  A equipe WebView tenta limitar o número de versões com alterações significativas.  Conforme a disponibilidade geral se aproxima, várias alterações significativas são incorporadas na versão Beta.  

*   > [!IMPORTANT]
    > **Alteração**de Alteração: conforme a versão final se aproxima, a equipe WebView renomeou o prefixo *IWebView2WebView para* *ICoreWebView2*   para garantir que a API WebView2 se alinhe com a convenção de nomenal da API do Windows.  Além disso, para aproveitar o SDK webView2 das estruturas da interface do usuário, a equipe WebView separada em `ICoreWebView2` [ICoreWebView2][ReferenceWin32Icorewebview209430] e [ICoreWebView2Host][ReferenceWin32Icorewebview2host09430].  `ICoreWebView2Host` dá suporte a resizing, showing-and-hiding, focusing e outras funcionalidades relacionadas à janela e à composição.  O ICoreWebView2 dá suporte a todas as outras funcionalidades WebView2.  Para saber mais sobre como incorporar as alterações, navegue até a solicitação pull [WebView2][GithubMicrosoftedgeWebview2samplesPr17] no projeto WebView2 [APISample.][GithubMicrosoftedgeWebview2samplesMain]  
    
*   > [!IMPORTANT]
    > **Alteração de**Quebra : Dividir [DocumentStateChanged][ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190] em três componentes:  [SourceChanged][ReferenceWin32Icorewebview2AddSourcechanged09430], [ContentLoading][ReferenceWin32Icorewebview2AddContentloading09430]e [HistoryChanged][ReferenceWin32Icorewebview2AddHistorychanged09430].  Agora, quando a URL de origem altera o `SourceChanged` evento é executado.  Quando o estado do histórico é `HistoryChanged` alterado, o evento é executado.  O `ContentLoading` evento é executado antes do script inicial quando um novo documento está sendo carregado.  
    
*   Adicionado suporte para arquitetura ARM64.  
*   Adicionado suporte ao Painel de Entrada Suave \(SIP\) para dispositivos de tela touch.  
*   Adicionado suporte para Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 e Windows Server 2016.  
*   [NotifyParentWindowPositionChanged][ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430] adicionado para a barra de status seguir a janela no modo de janela.  Além disso, implemente a alteração no modo sem janela para que os recursos de acessibilidade funcionem.  
*   Adicionada [a configuração AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430] para controlar globalmente se uma página da Web pode ser acessada por qualquer objeto remoto.  Por padrão, está ligado, para que os objetos remotos adicionados por `AreRemoteObjectsAllowed` [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] sejam acessíveis na página da Web.  Quando `AreRemoteObjectsAllowed` está desligado, os objetos não são acessíveis na página da Web.  As alterações são aplicadas no próximo evento de navegação.  
*   Adicionada [a configuração IsZoomControlEnabled][ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430] para impedir que os usuários a impactem no zoom do WebView usando e `ctrl` + `+` `ctrl` + `-` \(ou `ctrl` + roda do mouse\).  O zoom ainda pode ser definido [usando put_ZoomFactor][ReferenceWin32Icorewebview2hostPutZoomfactor09430] quando a configuração está desligada.  
*   ZoomFactor alterado para se aplicar somente ao WebView atual.  Zoom changes to the current WebView don't affect other WebViews that you navigated to using the same site of origin.  Para obter mais informações, navegue [até get_ZoomFactor][ReferenceWin32Icorewebview2hostGetZoomfactor09430].  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   [SetBoundsAndZoomFactor adicionado.][ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]  Agora, você pode definir o fator de zoom e os limites de um WebView ao mesmo tempo.  
*   Evento [WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] adicionado.  Para obter mais informações, [navegue até add_WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Adicionado suporte para o tipo de caixa de diálogo para eventos de caixa de diálogo `beforeunload` JavaScript e adicionado [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430] entrada de enum.  
*   [GetHeaders adicionados][ReferenceWin32Icorewebview2httprequestheadersGetheaders09430] a HttpRequestHeaders, [GetHeader][ReferenceWin32Icorewebview2httpresponseheadersGetheader09430] a HttpResponseHeaders [e][ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430] get_HasCurrentHeader propriedade a HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Alteração de Alteração:** Comportamento `DevToolsProtocolEventReceived` modificado.  Agora, você pode criar um [DevToolsProtocolEventReceiver][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430] para um evento específico do Protocolo DevTools e inscrever/cancelar a assinatura para esse evento usando o [add_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430] / [remove_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430].  
    
*   > [!IMPORTANT]
    > **Alteração de**Quebra: `WebMessageReceivedEventArgs` [alterou get_WebMessageAsString][ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190] propriedade para [um método TryGetWebMessageAsString.][ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]  
    
*   > [!IMPORTANT]
    > **Alteração de quebra:** `AcceleratorKeyPressedEventArgs` [alterou o método Handle][ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190] para [uma get_Handled][ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430] propriedade.  
    
## 0.8.355  

[Pacote NuGet][NuGetGallery0.8.355] \| Microsoft Edge versão 80.0.355.0.  

*   Lançamento do Exemplo de WebView2API, um guia abrangente do SDK webView2.  Para obter mais informações, navegue até [o exemplo de API.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Adicionado suporte a IME para todos os idiomas além do inglês \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Atualizou a superfície de API do `WebResourceRequested` evento em resposta a relatórios de bugs.  A especificação simultânea de um filtro e um evento na criação foi preterida.  Para criar um evento solicitado de recurso da [Web,][ReferenceWin32Iwebview2webview5AddWebresourcerequested08190] use add_WebResourceRequested para adicionar o evento e [AddWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190] para adicionar um filtro.  [RemoveWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190] remove o filtro \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Alteração Desaprimada:** Modificado o comportamento de tela inteira.  Preterido [IsFullScreenAllowed][ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190].  Agora, por padrão, se um elemento em um WebView \(como um vídeo\) estiver definido como tela inteira, ele preencherá os limites do WebView.  Use o [evento ContainsFullScreenElementChanged][ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190] [e][ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190] get_ContainsFullScreenElement para especificar como o aplicativo deve reencaminhar o WebView se um elemento quiser entrar no modo de tela inteira.  
    
## 0.8.314  

[Pacote NuGet][NuGetGallery0.8.314] \| Microsoft Edge versão 80.0.314.0.  

*   Adicionado suporte para Windows 7, Windows 8 e Windows 8.1.  
*   Adicionado o suporte de depuração do Visual Studio e do Visual Studio Code para WebView2.  Agora, depure seu script no WebView2 a partir do IDE.  Para obter mais informações, [navegue até Como depurar ao desenvolver com controles WebView2][HowtoDebug].  
*   Adicionado para o script em execução em WebView2 para acessar um objeto IDispatch do componente Win32 do aplicativo e acessar as propriedades do objeto `Native Object Injection` IDispatch.  Para obter mais informações, [navegue até AddRemoteObject][ReferenceWin32Iwebview2webview4Addremoteobject08190] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Evento `AcceleratorKeyPressed` adicionado.  Para obter mais informações, [navegue até add_AcceleratorKeyPressed][ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Desligado o `Context Menus` .  Para obter mais informações, [navegue até put_AreDefaultContextMenusEnabled][ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   `DPI Awareness`Atualizado.  Agora, o reconhecimento de DPI do WebView é o mesmo que o reconhecimento de DPI do aplicativo host.  
    
    > [!NOTE]
    > Se outro aplicativo híbrido for lançado com um Reconhecimento de DPI diferente do WebView original, o novo WebView não será lançado se for o mesmo `user data folder` \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Atualizado para que WebView2 rejeite automaticamente solicitações de permissão de notificação solicitadas pelo conteúdo da `Notification Change Behavior` Web hospedado no WebView.  
    
## 0.8.270  

[Pacote NuGet][NuGetGallery0.8.270] \| Microsoft Edge versão 78.0.270.0.  

*   Evento `DocumentTitleChanged` adicionado para indicar a alteração de título do documento \([\#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   A `GetWebView2BrowserVersionInfo` API foi adicionada \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Evento `NewWindowRequested` adicionado.  
*   Função `CreateWebView2EnvironmentWithDetails` atualizada para `releaseChannelPreference` remover.  Para obter mais informações sobre `CreateWebView2EnvironmentWithDetails` a função, navegue até [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  A substituição da variável do registro e do ambiente ainda é suportada.  A preferência de canal padrão é usada, a menos que seja substituído.  
    Durante a pesquisa de canal, a equipe WebView ignora qualquer versão de canal anterior que não seja compatível com o SDK WebView2.  
    A equipe WebView seleciona o canal mais estável para garantir os comportamentos mais consistentes para o usuário final.  Ao testar com as versões mais recentes do Canary, você deve criar um script para definir a variável de ambiente `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` antes de iniciar o `1` aplicativo.  
*   Atualizou `CreateWebView2EnvironmentWithDetails` a função com lógica para seleção quando não `userDataFolder` especificado.  Para obter mais informações sobre `CreateWebView2EnvironmentWithDetails` a função, navegue até [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Se você usou o local padrão anteriormente, ao alternar para o novo SDK, o padrão será redefinido \(definido como um novo local no diretório de código de host\) e seu estado também será `userDataFolder` `userDataFolder` redefinido.  Se o processo de host não tiver permissão para gravar no diretório especificado, a `CreateWebView2EnvironmentWithDetails` função poderá falhar.  Você pode copiar os dados do antigo `user data folder` para o novo diretório.  
    
## 0.8.230  

[Pacote NuGet][NuGetGallery0.8.230] \| Microsoft Edge versão 77.0.230.0.  

*   Api `Stop` adicionada para interromper toda a navegação e buscas de recursos pendentes \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Arquivo `.tlb` adicionado ao pacote NuGet \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Adicionados projetos .NET à lista de instalador no pacote NuGet \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  
    
## 0.8.190  

[Pacote NuGet][NuGetGallery0.8.190] \| Microsoft Edge versão 77.0.190.0.  

*   Adicionado `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` para controlar se os usuários podem abrir o DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Adicionado `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` para controlar se a barra de status é exibida \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Adicionado `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` para voltar e avançar no histórico de navegação.  
*   Foram adicionados tipos de cabeçalho HTTP \( \) para exibição e modificação de `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` cabeçalhos HTTP no WebView.  
*   Adicionado suporte a WebView de 32 bits em máquinas de 64 bits \([\#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   IDL do WebView adicionada ao SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Foi adicionada a biblioteca para `IID\_\*` dar suporte a objetos de ID de interface \([\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Adicionado incluem caminho, vinculação e autocópia de arquivos DLL para o arquivo NuGet `TARGET` no SDK.  
*   A solicitação está `window.open()` 100% em script.  
    
## 0.8.149  

[Pacote NuGet][NuGetGallery0.8.149] \| Microsoft Edge versão 76.0.149.0.  

Versão inicial da visualização do desenvolvedor.  

<!-- Links -->  

[VersioningDoc]: ./concepts/versioning.md#matching-webview2-runtime-versions
[ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando WebView2 | Microsoft Docs"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Modo de distribuição evergreen - distribuição de aplicativos usando WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Modo de distribuição de Versão Fixa - Distribuição de aplicativos usando WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Compreender o Instalador e o Tempo de Execução do WebView2 - Distribuição de aplicativos usando o WebView2 | Microsoft Docs"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Políticas de grupo para WebView2 - Gerenciando aplicativos WebView2 | Microsoft Docs"  
[ConceptsVersioning]: ./concepts/versioning.md "Noções básicas sobre versões de navegador e webview2 | Microsoft Docs"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "APIs experimentais - Noções básicas sobre versões de navegador e webview2 | Microsoft Docs"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Getting started with WebView2 in Windows Forms apps | Microsoft Docs"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Getting started with WebView2 in WPF | Microsoft Docs"  
[HowtoDebug]: ./howto/debug.md "Como depurar ao desenvolver com controles WebView2 | Microsoft Docs"  

[ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Alça - interface IWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs"  
[ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interface IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft Docs"  
[ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled - interface IWebView2Settings2 | Microsoft Docs"  
[ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated - interface IWebView2Settings | Microsoft Docs"  
[ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString - interface IWebView2WebMessageReceivedEventArgs | Microsoft Docs"  
[ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed - interface IWebView2WebView4 | Microsoft Docs"  
[ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged - interface IWebView2WebView | Microsoft Docs"  
[ReferenceWin32Iwebview2webview4Addremoteobject08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject - interface IWebView2WebView4 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5AddWebresourcerequested08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested - interface IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter - interface IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement - interface IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter - interface IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails - Globals | Microsoft Docs"  

[ReferenceWin32Icorewebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled - interface ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddContentloading09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddHistorychanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2Addremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddSourcechanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddWindowcloserequested09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived - interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived - interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo - interface ICoreWebView2Environment | Microsoft Docs"  
[ReferenceWin32Icorewebview2host09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo - Globals | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostGetZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor - interface ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged - interface ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostPutZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor - interface ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor - interface ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader - interface ICoreWebView2HttpHeadersCollectionIterator | Microsoft Docs"  
[ReferenceWin32Icorewebview2httprequestheadersGetheaders09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders - interface ICoreWebView2HttpRequestHeaders | Microsoft Docs"  
[ReferenceWin32Icorewebview2httpresponseheadersGetheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader - interface ICoreWebView2HttpResponseHeaders | Microsoft Docs"  
[ReferenceWin32Icorewebview2Removeremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - interface ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled - interface ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString - interface ICoreWebView2WebMessageReceivedEventArgs | Microsoft Docs"  

[ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2Addhostobjecttoscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddNewwindowrequested09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentoptions09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2EnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Microsoft Docs"
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalpointerinfo09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalPointerInfo | Microsoft Docs"  
[ReferenceWin32Icorewebview2Removehostobjectfromscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - interface ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Microsoft Docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails - Globals | Microsoft Docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString - Globals | Microsoft Docs"  

[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged - interface ICoreWebView2ExperimentalController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode - interface ICoreWebView2ExperimentalController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale - interface ICoreWebView2ExperimentalController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges - interface ICoreWebView2ExperimentalController | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft.Web.WebView2.Core | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft.Web.WebView2.WinForms | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Classe CoreWebView2 (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Classe CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Método CoreWebView2Environment.CompareBrowserVersions(String, String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Método CoreWebView2Environment.GetAvailableBrowserVersionString(String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Evento CoreWebView2.NewWindowRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Evento CoreWebView2.PermissionRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Evento CoreWebView2.ScriptDialogOpening (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Evento CoreWebView2.WebResourceRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Classe CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Classe CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Classe CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Classe Webview2.Source (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Método WebView2.BuildWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Método WebView2.DestroyWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Classe CoreWebView2InitializationCompletedEventArgs | Microsoft Docs"  

[ReferenceWin32Icorewebview2Addhostobjecttoscript09538]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript - interface ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled - interface ICoreWebView2ExperimentalEnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures - interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWindowFeatures | Microsoft Docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated interface ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed - interface ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs"  

[ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount - interface ICoreWebView2EnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments - interface ICoreWebView2EnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures - interface ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2windowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interface ICoreWebView2WindowFeatures | Microsoft Docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Edge"  
[ReferenceWin32Icorewebview2experimentalenvironment09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.628-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalEnvironment | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft Docs"  

[ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - interface ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalGetCookiemanager10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager - interface ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalGetEnvironment10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment - interface ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest - interface ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2#get_systemcursorid?view=webview2-1.0.674-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent - interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs"  

[ReferenceWin32Icorewebview2experimentalcompositioncontroller3]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController3 | Microsoft Docs"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 - Políticas | Microsoft Docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender Application Guard (Windows 10) - segurança do Windows | Microsoft Docs"

[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Classe CancelEventArgs (System.ComponentModel) | Microsoft Docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Classe EventArgs (System) | Microsoft Docs"  
[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblies com nome forte | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Comentários sobre o MicrosoftEdge/WebViewFeedback Problema 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Comentários sobre o MicrosoftEdge/WebViewFeedback Problema 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Comentários sobre o MicrosoftEdge/WebViewFeedback Problema 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 108"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 119"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 131"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 177"
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 185"
[GithubMicrosoftedgeWebviewfeedbackIssue204]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 204"
[GithubMicrosoftedgeWebviewfeedbackIssue219]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 219"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 235"
[GithubMicrosoftedgeWebviewfeedbackIssue250]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 250"
[GithubMicrosoftedgeWebviewfeedbackIssue288]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 288"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 611"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]:  https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Comunicado de repo para MicrosoftEdge/WebViewAnnouncement Problema 2"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Mover o projeto para usar o SDK 0.9.430 - MicrosoftEdge/WebView2Samples mais | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemplo de API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Anúncio da disponibilidade geral do Microsoft Edge WebView2 para .NET e método de distribuição fixa | blog .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Desenvolvedor do Microsoft Edge"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Galeria NuGet | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galeria NuGet | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galeria NuGet | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galeria NuGet | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galeria NuGet | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galeria NuGet | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galeria NuGet | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galeria NuGet | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galeria NuGet | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galeria NuGet | Pré-lançamento do Microsoft.Web.WebView2 v0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galeria NuGet | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Galeria NuGet | Microsoft.Web.WebView2 v0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Galeria NuGet | Microsoft.Web.WebView2 v0.9.622.11"
[NuGetGallery1.0.622.22]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Galeria NuGet | Microsoft.Web.WebView2 v1.0.622.22"
[NuGetGallery1.0.664.34]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Galeria NuGet | Microsoft.Web.WebView2 v1.0.664.34"
[NuGetGallery1.0.664.37]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Galeria NuGet | Microsoft.Web.WebView2 v1.0.664.37"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Galeria NuGet | Pré-lançamento do Microsoft.Web.WebView2 v0.9.628"  
[NuGetGallery1.0.674-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Galeria NuGet | Pré-lançamento do Microsoft.Web.WebView2 v1.0.674"  
[NuGetGallery1.0.721-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "Galeria NuGet | Pré-lançamento do Microsoft.Web.WebView2 v1.0.721"  
[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Anúncio da Disponibilidade Geral do Microsoft Edge WebView2 | Microsoft Edge Blog"  

[WebResourceResponseReceivedAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#add_webresourceresponsereceived&preserve-view=true "add_WebResourceResponseReceived - interface ICoreWebView2 | Microsoft Docs"
[NavigateWithWebResourceRequestAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease#createwebresourcerequest&preserve-view=true "CreateWebResourceRequest - interface ICoreWebView2Environment | Microsoft Docs"
[CookiemanagementAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs"
[DOMContentLoadedAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#add_domcontentloaded&preserve-view=true "add_DOMContentLoaded - interface ICoreWebView2_2 | Microsoft Docs"
[WebViewEnvironmentproperty]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#get_environment&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs"

[GithubMicrosoftedgeWebviewfeedbackIssue58]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 58" 
[GithubMicrosoftedgeWebviewfeedbackIssue122]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 122" 
[GithubMicrosoftedgeWebviewfeedbackIssue196]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 196" 
[GithubMicrosoftedgeWebviewfeedbackIssue399]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 399" 
[GithubMicrosoftedgeWebviewfeedbackIssue400]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 409" 
[GithubMicrosoftedgeWebviewfeedbackIssue605]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 691" 
[GithubMicrosoftedgeWebviewfeedbackIssue414]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 414" 
[NuGetGallery1.0.705.50]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "Galeria NuGet | Microsoft.Web.WebView2 v1.0.705.50"
[NuGetGallery1.0.781-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.781-prerelease "Galeria NuGet | Pré-lançamento do Microsoft.Web.WebView2 v1.0.781"  
[ReferenceWin32Icorewebview210781PreReleaseTrySuspendResume]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.781-prerelease&preserve-view=true#TrySuspend "TrySuspend - interface ICoreWebview2_3 | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalsettings10781PreReleaseGetUserAgent]: /microsoft-edge/webview2/reference/win32/icorewebview2/icorewebview2experimentalsettingsget_useragent "get_UserAgent - interface ICoreWebView2ExperimentalSettings | Microsoft Docs"  
[ReferenceWin32Icorewebview210781PreReleaseSetVirtualHostNameToFolderMapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.781-prerelease&preserve-view=true#SetVirtualHostNameToFolderMapping "SetVirtualHostNameToFolderMapping - interface ICoreWebView2_3 | Microsoft Docs"   
[ReferenceWin32Icorewebview2controllerViewWebview210781PreReleaseDefaultBackgroundColor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller?view=webview2-1.0.781-prerelease&preserve-view=true#defaultbackgroundcolor "DefaultBackgroundColor - interface ICoreWebView2Controller2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2controllerViewWebview210781CompositionController]:  /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.781-prerelease&preserve-view=true "interface ICoreWebView2CompositionController | Microsoft Docs"  
[ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerInvoke10781]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.781-prerelease&preserve-view=true#invoke "Invoke - interface ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Microsoft Docs"  
