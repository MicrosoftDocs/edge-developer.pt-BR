---
description: Notas de versão para Microsoft Edge SDK WebView2
title: Notas de versão para Microsoft Edge WebView2 para Win32, WPF e WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, controle de navegador, html de borda
ms.openlocfilehash: 63a81baed1f4b67cf37b95fa88abd0b6f67b1e4d
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536273"
---
# <a name="release-notes-for-webview2-sdk"></a>Notas de versão do SDK WebView2  

A equipe webView2 atualiza o [SDK WebView2][NuGetGallery] em uma cadência de seis semanas.  Revise o conteúdo a seguir para obter informações atualizadas sobre anúncios de produtos, adições, modificações e alterações de quebra nas APIs.  

> [!NOTE]
> Certifique-se de compilar seu aplicativo depois de atualizar o NuGet pacote.  A equipe webView recomenda que você use o canal Canary ao desenvolver usando os pacotes de pré-lançamento e o Evergreen WebView2 Runtime ao usar os pacotes de versão.  Para obter mais informações, navegue até [Matching WebView2 Runtime versions][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions].  

> [!NOTE]
> As correções de bugs do WebView2 são específicas do Tempo de Execução ou do SDK.  

## <a name="10865-prerelease"></a>1.0.865-prerelease  

Data de lançamento: 26 de abril de 2021  

[NuGet pacote][NuGetGallery1.0.865-prerelease] \| Versão Microsoft Edge mínima para carregar: 86.0.616.0 ou mais recente \| Compatibilidade completa da API: 91.0.865.0 ou mais nova  

### <a name="general"></a>Geral  

#### <a name="experimental-features"></a>Recursos experimentais  

*   Foi [adicionada a configuração IsPinchZoomEnabled.][Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled] Ele permite ativar ou desativar o controle de zoom de escala de página em uma configuração.  
*   Adicionada a [API add_DownloadStarting][Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting] Personalizada.  Ele permite bloquear downloads, salvar em um caminho diferente e acessar os metadados necessários para criar a interface do usuário de download personalizada.  
*   Adicionado `iframe` suporte a elemento de [AddHostObjectToScriptWithOrigins][Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins].  
*   Adicionado código de exemplo para [o aplicativo de exemplo WPF][GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser] para usar a API para desativar as teclas de função do navegador.  
*   Adicionada a API [UpdateRuntime,][Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime] para atualizar facilmente o Tempo de Execução do WebView2.  
    
#### <a name="bug-fixes"></a>Correções de bugs  

*   Manipulador fixo para uma `Chromium DevTools Protocol` mensagem com `POST` dados binários no WebView2.  
*   A interface do `OpenSaveAsAwareness` usuário de download foi desligada, pois incluía links para `edge://settings` .  \([\#1120][GithubMicrosoftedgeWebviewfeedbackIssue1120]\).  
*   Removeu a identidade visual da caixa de diálogo compartilhamento de tela.  \([\#940][GithubMicrosoftedgeWebviewfeedbackIssue940]\).  
*   Correção de bug em [que a função SetWindowDisplayAffinity][WindowsWin32ApiWinuserSetWindowDisplayAffinity] quebrava o WebView2 quando interrompeu a captura de tela em um aplicativo WebView2.  \([\#841][GithubMicrosoftedgeWebviewfeedbackIssue841]\).
*   Erro corrigido para hospedagem de composição onde a entrada do mouse parou de funcionar se qualquer entrada de caneta foi enviada para WebView2.  
*   Erro corrigido que interrompeu a entrada do mouse após qualquer entrada de caneta.  Essa alteração é específica do Tempo de Execução.  
    
### <a name="net"></a>.NET  

#### <a name="experimental-features"></a>Recursos experimentais  

*   Adicionada a ferramenta de designer WebView2 à Caixa de Ferramentas WPF.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Adicionado elemento de interface do usuário webView2 no modo de designer .NET.  
    
#### <a name="bug-fixes"></a>Correções de bugs  

*   Descrições de exceção COM aprimoradas envolvendo cada uma delas em uma exceção .NET mais detalhada.  \([\#338][GithubMicrosoftedgeWebviewfeedbackIssue338]\).  Essa alteração é específica do Tempo de Execução.  
*   Erro corrigido causado quando você seleciona a mudança de foco fez com que o controle WebView2 falha Microsoft Visual Studio `tab` Ferramentas para Office.  \([\#589][GithubMicrosoftedgeWebviewfeedbackIssue589] e [\#933][GithubMicrosoftedgeWebviewfeedbackIssue933]\).  Essa alteração é específica do Tempo de Execução.  
*   Nível inferior do carregador de estrutura .NET aprimorado para ser mais robusto.  \([\#946][GithubMicrosoftedgeWebviewfeedbackIssue946]\).
*   Erro corrigido que causou falha ao tentar atualizar antes da primeira navegação ser concluída.  \([\#1011][GithubMicrosoftedgeWebviewfeedbackIssue1011]\).
*   Inicialização fixa para que a navegação ocorra durante `CoreWebView2InitializationCompleted` .  \([\#1050][GithubMicrosoftedgeWebviewfeedbackIssue1050]\).
*   Tratamento de erro de falha do processo do navegador .NET aprimorado.  Agora você pode recriar controles depois de manipular um `ProcessFailed` evento sem uma falha.  \([\#996][GithubMicrosoftedgeWebviewfeedbackIssue996]\).  

## <a name="1081841"></a>1.0.818.41  

Data de lançamento: 21 de abril de 2021  

[NuGet pacote][NuGetGallery1.0.818.41] \| Versão mínima do Tempo de Execução a ser carregada: 86.0.616.0 ou mais recente \| Compatibilidade completa da API: 90.0.818.41 ou mais nova  

### <a name="general"></a>Geral  

#### <a name="features"></a>Recursos  

*   Código WebView2 aprimorado para ser mais resiliente aos arquivos `.exe` de aplicativos com informações de versão malformadas.  \([\#850][GithubMicrosoftedgeWebviewfeedbackIssue850]\).  
*   Removida `--winhttp-proxy-resolver` da linha de comando do processo do navegador WebView, ativas outras opções de linha de comando proxy para WebView2.  
  
## <a name="10824-prerelease"></a>1.0.824-prerelease  

Data de lançamento: 8 de março de 2021  

[NuGet pacote][NuGetGallery1.0.824-prerelease] \| Versão Microsoft Edge mínima para carregar: 86.0.616.0 ou mais recente \| Compatibilidade completa da API: 91.0.824.0 ou mais nova  

### <a name="general"></a>Geral  

#### <a name="features"></a>Recursos  

*   Estendeu o `ProcessFailed` evento.  Agora eleva para processos filho não renderadores e renderistas de quadro.  
*   Adicionada a [configuração experimental AreBrowserAcceleratorKeysEnabled.][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]  Você pode impedir que o navegador responde a atalhos de teclado relacionados à navegação, impressão, salvação e outras funções específicas do navegador.  
*   Adicionado `iframe` suporte a elemento para `AddScriptToExecuteOnDocumentCreated` .  
    
#### <a name="promotion"></a>Promoção  

*   [UserAgent][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] A API agora é promovida para Estável.  
*   As APIs da Escala de Rasterização \([Propriedade RasterizationScale,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]  [evento RasterizationScaleChanged,][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] [propriedade BoundsMode][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]e [propriedade ShouldDetectMonitorScaleChanges\)][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] agora são promovidas para Estável.  
    
#### <a name="bug-fixes"></a>Correções de bugs  

*   Tipos de projeto C++ e .NET com suporte expandido, como MFC e ATL.  \([\#506,][GithubMicrosoftedgeWebviewfeedbackIssue506] [\#669][GithubMicrosoftedgeWebviewfeedbackIssue669]e [\#851][GithubMicrosoftedgeWebviewfeedbackIssue851]\).  
*   Correção de um bug que o Evergreen WebView2 Runtime vaza a entrada do firewall de entrada.  
*   Configuração fixa Resposta durante `WebResourceRequested` o evento.  \([\#568][GithubMicrosoftedgeWebviewfeedbackIssue568]\).  
*   Correção de um bug que navega para fazer com `edge://` que o processo do navegador saia.  \([\#604][GithubMicrosoftedgeWebviewfeedbackIssue604]\).  
*   Correção de um bug que limitava WebView2 ao tamanho da tela no modo de Hospedagem Visual.  

## <a name="1077444"></a>1.0.774.44  

Data de lançamento: 8 de março de 2021  

[NuGet pacote][NuGetGallery1.0.774.44] \| Versão mínima do Tempo de Execução a ser carregada: 86.0.616.0 ou mais recente \| Compatibilidade completa da API: 89.0.774.44 ou mais nova  

### <a name="general"></a>Geral  

#### <a name="features"></a>Recursos  

*   Desligou vários Microsoft Edge de navegador no WebView2.  
*   As APIs de Hospedagem Visual agora estão geralmente disponíveis.  

#### <a name="promotions"></a>Promoções  

*   As APIs experimentais a seguir agora são promovidas para Estável.  
    *   Suporte a APIs relacionadas ao [DPI][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   APIs de hospedagem visual  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend e Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
        
#### <a name="bug-fixes"></a>Correções de bugs  

*   Correção de um bug que limitava WebView2 ao tamanho da tela no modo de Hospedagem Visual.  
    
## <a name="10790-prerelease"></a>1.0.790-prerelease  

Data de lançamento: 10 de fevereiro de 2021  

[NuGet pacote][NuGetGallery1.0.790-prerelease] \| Microsoft Edge versão 86.0.616.0 ou mais recente  

### <a name="general"></a>Geral  

> [!IMPORTANT]
> **Alteração de**quebra : o pacote de pré-lançamento do WebView2 1.0.781 está preterido.  Interrompa o desenvolvimento com o pacote 1.0.781.  

> [!IMPORTANT]
> O pacote de pré-lançamento do WebView2 0.9.430 está preterido e é removido com a próxima versão.  Se o aplicativo WebView usar o pacote, a equipe do WebView recomenda que você mude para um pacote mais novo.  

#### <a name="features"></a>Recursos  

*   Adicionado [o método TrySuspend e Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] para suspender e retomar WebViews.  
*   Adicionado [o método SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] que mapeia um nome de host virtual para um caminho de diretório.  \([\#37][GithubMicrosoftedgeWebviewfeedbackIssue37], [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]e [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   A propriedade [DefaultBackgroundColor foi adicionada][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] para definir a cor e o canal alfa do plano de fundo.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Adicionada a [propriedade UserAgent][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] para obter ou definir o Agente de Usuário.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Substituiu o `CreateCookieWithCookie` método pelo `CopyCookie` método.  
*   Adicionado suporte de hospedagem visual usando a interface [ICoreWebView2CompositionController,][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] que é criada usando o novo `CreateCoreWebView2CompositionController` método de `ICoreWebView2Environment3` .  
    
#### <a name="bug-fixes"></a>Correções de bugs  

*   Foi desligado o recurso Microsoft Edge Compras no WebView2.  
*   Desligado o menu de contexto no visualizador PDF quando `AreDefaultContextMenusEnabled` for `false` .  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Correção de um bug que `E_NOINTERFACE` retornou ao consultar `ICoreWebView2` `ICoreWebView2Experimental` .  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Correção de um bug que permitia a navegação com URIs malformadas quando `CoreWebView2NavigationStartingEventArgs.Cancel` definido como `false` .  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Correção de um bug bloqueado `window.print()` em janelas pop-up com manipuladores de eventos anexados a `NewWindowRequested` eventos.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Corrigido o problema de DPI dinâmico ao mover aplicativos entre monitores diferentes.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Aprimorou as `HRESULT` instâncias passadas por [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke].  
*   Botão de gerenciamento de preenchimento automático desligado.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Correção Visual Studio falhas enquanto você `WebView2.Dispose` é executado quando hospedado em várias janelas.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\) e [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Erro corrigido para exibir o controle WebView2 na Visual Studio Toolbox.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Redução dos altos problemas de uso da CPU.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Corrigidos problemas com o pacote 1.0.781-pre-release pre-lançamento preterido.  \([\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] e [\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
#### <a name="promotions"></a>Promoções  

*   As APIs experimentais a seguir agora são promovidas para Estável.  
    *   APIs de Hospedagem Visual  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
        
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Correções de bugs  

*   Bug corrigido que despencou aplicativos WebView que usam o SDK WPF.  A falha ocorreu quando você `F4` selecionou para fechar uma janela.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   A tela de inicialização do WebView2 agora é transparente, em vez de cinza.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## <a name="1070550"></a>1.0.705.50  

Data de lançamento: 25 de janeiro de 2021  

[NuGet pacote][NuGetGallery1.0.705.50] \| WebView2 Runtime versão 86.0.616.0 ou mais recente  

### <a name="general"></a>Geral  

#### <a name="promotions"></a>Promoções  

*   As APIs experimentais a seguir agora são promovidas para Estável.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API de gerenciamento de cookies][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Propriedade WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  

## <a name="10721-prerelease"></a>1.0.721-prerelease  

Data de lançamento: 8 de dezembro de 2020  

[NuGet pacote][NuGetGallery1.0.721-prerelease] \| Microsoft Edge versão 86.0.616.0 ou mais recente  

### <a name="general"></a>Geral  

> [!IMPORTANT]
> **Alteração de**quebra : o pacote de pré-lançamento do WebView2 1.0.707 e o pacote 0.9.628 estão preterido.  Interrompa o desenvolvimento com o pacote 1.0.707 e o package0.9.628.  

#### <a name="features"></a>Recursos  

*   Foram [adicionadas políticas de grupo WebView2.][DeployedgeMicrosoftEdgeWebviewPolicies]  Para obter mais informações sobre as práticas recomendadas, navegue até [políticas de grupo para WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Alteração de Quebra**: preterido o local antigo do Registro.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Adicionado suporte para [Arrastar e Soltar][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] no WebView2.  
*   Adicionadas APIs para lidar com o suporte a DPI.  
    *   Adicionada [a propriedade RasterizationScale][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] para alterar a escala DPI para conteúdo WebView e pop-ups de interface do usuário e evento [RasterizationScaleChanged][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] associado.  
    *   Adicionada [a propriedade ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] para atualizar automaticamente a `RasterizationScale` propriedade, se necessário.  
    *   A [propriedade BoundsMode][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] foi adicionada para especificar que os limites são pixels lógicos e permitir que o WebView use para exibição `RasterizationScale` de pixels WebView2 e WebView use o com o para obter o `RasterizationScale` tamanho `Bounds` físico.  
*   Evento `NewWindowRequested` atualizado para manipular e `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] e [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   As APIs experimentais a seguir agora são promovidas para Estável.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API de gerenciamento de cookies][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Propriedade WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
### <a name="net"></a>.NET  

#### <a name="features"></a>Recursos  

*   A turned on WinForms designer in .NET Core 3.1+ and .NET 5.  
*   Gerenciamento de cookies .NET aprimorado.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Substituído por `CoreWebView2Ready` [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  

#### <a name="bug-fixes"></a>Correções de bugs

*   Adicionado [evento AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] para dar `AcceleratorKey` suporte à seleção no WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Removidos arquivos desnecessários de serem saídas para pastas WebView2.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   API de objeto host aprimorada.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] e [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## <a name="1066437"></a>1.0.664.37  

Data de lançamento: 20 de novembro de 2020  

[NuGet pacote][NuGetGallery1.0.664.37] \| WebView2 Runtime versão 86.0.616.0 ou mais recente  

### <a name="general"></a>Geral  

> [!IMPORTANT]
> **Comunicado**: .NET WPF/WinForms WebView2 SDKs agora estão geralmente disponíveis \(GA\).  A partir dessa versão, os SDKs de versão são compatíveis com encaminhamento.  Para obter mais detalhes, navegue até [Ga announcement blog post][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod].  

#### <a name="features"></a>Recursos  

*   O .NET WPF/WinForms WebView2 agora está geralmente disponível \(GA\).  
*   O modo Distribuição Fixa \(Bring-your-own\) atingiu GA.  
    
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Correções de bugs  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` impede que a nova janela seja aberta.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] e [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## <a name="10674-prerelease"></a>1.0.674-prerelease  

Data de lançamento: 19 de outubro de 2020  

[NuGet pacote][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime versão 86.0.616.0 ou mais recente  

### <a name="general"></a>Geral  

*   Foi [adicionado o método NavigateWithWebResourceRequest][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] para fornecer dados postados ou outros headers de solicitação durante a navegação.  
*   Adicionado [evento DOMContentLoaded][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] que é executado quando o documento HTML inicial é carregado e analisado.  
*   Adicionada a [propriedade Environment][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] no WebView2.  Essa propriedade expõe o ambiente WebView2 onde uma instância do WebView2 foi criada.  
*   Foram [adicionadas][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] APIs de gerenciamento de cookies que permitem aos desenvolvedores autenticar a sessão WebView2 ou recuperar cookies do WebView para autenticar outras ferramentas.  A equipe do Webview planeja fazer melhorias específicas do idioma ou da estrutura.  Para obter mais informações, navegue até [Análise da API: Gerenciamento de Cookies][GithubMicrosoftedgeWebview2AnnouncementIssue2].  
*   Atualizou o [evento WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] e adicionou [WebResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] imutável e [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] a [WebResourceResponseView::GetContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent].  
*   Desligado Microsoft Defender Application Guard [(WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] no WebView2.  
*   Adicionado [SystemCursorId][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] para Hospedagem Visual.  
*   Adicionado bug corrigido para o Método de Entrada na Hospedagem Visual.  
*   Removido incluem `version.lib` requisitos para ao usar a biblioteca estática WebView2.  
    
### <a name="net"></a>.NET  

*   Classe [CoreWebView2 atualizada][DotnetApiMicrosoftWebWebview2CoreCorewebview2] para expor a `CoreWebView2Environment` variável.  
*   Implementações alteradas das classes EventArgs personalizadas no namespace para `Microsoft.Web.WebView2.Core` subclasses [de System.EventArgs][DotnetApiSystemEventargs] ou [System.ComponentModel.CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Adicionado suporte para [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] em WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   Foram adicionadas APIs .NET adicionadas [WebResourceRequested.][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Propriedade WinForms Designer [Source][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] atualizada como padrão ou redefinida como null.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Limites do WebView2 atualizados em WebView2.Init() para dar suporte a modos DPI com menos de 100%.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   [BuildWindowCore e][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] atualizados para aumentar a robustez.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Base atualizada do Carregador .NET para carregar no bit do processo em vez da arquitetura do sistema operacional.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Renomeado `EdgeNotFoundException` para [WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## <a name="1062222"></a>1.0.622.22  

Data de lançamento: 19 de outubro de 2020  

[NuGet pacote][NuGetGallery1.0.622.22] \| WebView2 Runtime versão 86.0.616.0 ou mais recente  

### <a name="general"></a>Geral  

> [!IMPORTANT]
> **Comunicado**: Win32 C/C++ WebView2 agora está geralmente disponível \(GA\).  A partir desta versão, os SDKs de versão são compatíveis com encaminhamento.  Para obter mais informações, navegue até [ga postagem de blog de anúncio][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability].  

*   [Evergreen WebView2 Runtime e installer][Webview2ConceptsDistributionUnderstandRuntimeInstaller] são GA.  Bootstrapper, link de downlink para o Bootstrapper e o Instalador Autônomo para o Evergreen WebView2 Runtime estão disponíveis em [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  O código de exemplo para o fluxo de trabalho de instalação também está disponível no [repo WebView2Samples.][GithubMicrosoftedgeWebview2samplesMain]  
*   [O modo Versão Fixa][Webview2ConceptsDistributionFixedVersionDistributionMode] está disponível para visualização do desenvolvedor.  
    
## <a name="0962211"></a>0.9.622.11  

Data do lançamento: 10 de setembro de 2020  

[NuGet pacote][NuGetGallery0.9.622.11] \| WebView2 Runtime versão 86.0.616.0 ou mais recente  

### <a name="general"></a>Geral  

*   > [!IMPORTANT]
    > **Comunicado**: Este SDK é o Candidato de Lançamento para WebView2 Win32 C/C++ GA.  A versão GA deve usar a mesma interface e funcionalidade da API.  
    
*   Políticas de [navegador desconectadas][DeployedgeMicrosoftEdgePolicies].  
*   Adicionada [a propriedade AllowSingleSignOnUsingOSPrimaryAccount][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] nas opções de ambiente WebView2 para ativar o acesso condicional para WebView.  
*   Atualizado `ICoreWebView2NewWindowRequestedEventArgs` para incluir a propriedade [WindowFeatures][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] e o [ICoreWebView2WindowFeatures][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]associado.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Atualizado `System.Windows.Rect`  para uso em vez de `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Evento NewWindowRequested atualizado para manipular `window.open()` a solicitação sem parâmetros.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] especificado com não são substituídos por variáveis de ambiente `ICoreWebView2EnvironmentOptions` ou valores do Registro.  Para obter mais informações, navegue até [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions].  
    
## <a name="09579"></a>0.9.579  

Data de lançamento: 20 de julho de 2020  

[NuGet pacote][NuGetGallery0.9.579] \| Microsoft Edge versão 86.0.579.0.  

### <a name="general"></a>Geral  

*   > [!IMPORTANT]
    > **Comunicado**: Evergreen WebView2 Runtime and installer is released for preview.  Para obter mais informações, navegue até [Distribuição de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller].  
    
*   > [!IMPORTANT]
    > **Comunicado**: As seguintes versões do SDK webView2 não são mais suportadas após o próximo lançamento do SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > As versões do SDK webView2 também são marcadas preteridas nuget.org.  WebView2 recomenda manter-se atualizado com a versão mais recente do WebView2.  
    
*   Foram adicionadas melhorias no thread de trabalho do WebView.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Desligado o bloqueador pop-up no WebView.  Para obter mais informações, navegue até a [propriedade IsUserInitiated][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] no `NewWindowRequested` evento.  
*   Evento de início de navegação WebView garantido é executado para `about:blank` .  Agora, os eventos são executados para toda a navegação, mas os cancelamentos para ou do elemento não são suportados `NavigationStarting` `about:blank` e `srcdoc` `iframe` ignorados.  
*   `edge://`Bloqueei alguns esquemas de URI no WebView.  
*   Adicionada a propriedade experimental [IsSingleSignOnUsingOSPrimaryAccountEnabled][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] em opções de ambiente WebView2 para ativar o acesso condicional para WebView.  
*   Adicionado evento [experimental WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] que é executado depois que o WebView recebe e processa a resposta de uma solicitação webResource.  Os headers de autenticação, se algum, estão incluídos no objeto de resposta.  
    
### <a name="net"></a>.NET  

*   Melhor tratamento de foco WPF.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Propriedade `ZoomFactor` adicionada no controlador webview2 WPF.  
    
## <a name="09538"></a>0.9.538  

[NuGet pacote][NuGetGallery0.9.538] \| Microsoft Edge versão 85.0.538.0.  

### <a name="general"></a>Geral  

*   Soltar suporte para o SDK WebView2 Versão [0.8.149](#08149).  WebView2 recomenda manter-se atualizado com a versão mais recente do WebView2.  
*   Política de grupo atualizada para contabiliza quando o caminho de perfil do navegador Microsoft Edge é modificado \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
### <a name="win32-cc"></a>Win32 C/C++  

*   [ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures], que é a ser executado e associado ao `window.open()` [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Alteração de Quebra**: Preterido [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] e substituído por [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Alteração de**quebra : para garantir que a API WebView2 se alinhe com as convenções de nomenis da API Windows, a equipe do WebView atualizou os nomes dos seguintes.  
    > 
    > *   [AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] agora [é AreHostObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed].  
    
*   [AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]atualizado.  Os marcadores de serializador de objeto host originais agora estão definidos para os objetos proxy.  Em seguida, os marcadores de serializador de objeto host são serializados de volta como um objeto host quando passados como um parâmetro no retorno de chamada JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
### <a name="net-09538-pre-release"></a>.NET (0.9.538 pré-lançamento)  

*   WinForms e WPF WebView2API Samples lançados, que são guias abrangentes do SDK WebView2.  Para obter mais informações, navegue até [Amostras de Repo][GithubMicrosoftedgeWebview2samplesMain].  
*   Adicionado suporte para hospedagem visual e recursos de janela [apIs experimentais.][Webview2ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Alteração de**Quebra : os seguintes adiamentos agora implementam IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]e [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   Adicionado [GetAvailableBrowserVersionString e][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] como [coreWebView2Environment][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] estáticos.  
    
## <a name="09515-prerelease"></a>0.9.515-prerelease  

[NuGet pacote][NuGetGallery0.9.515-prerelease] \| Microsoft Edge versão 84.0.515.0.  

*   > [!IMPORTANT]
    > **Comunicado**: o WebView2 agora suporta Windows Forms e WPF no .NET Framework 4.6.2 ou posterior e .NET Core 3.0 ou posterior no pacote de **pré-lançamento**.  
    
*   Para obter mais informações sobre como criar aplicativos WPF, navegue até o Guia de Iniciação do [WPF][Webview2GettingstartedWpf] e a Referência [WPF][DotnetApiMicrosoftWebWebview2Wpf] webView2 para APIs específicas do WPF.  
*   Para obter mais informações sobre Windows aplicativos [][Webview2GettingstartedWinforms] de formulários, navegue até o Guia de Windows Formulários Windows e a Referência de Formulários Windows WebView2 [][DotnetApiMicrosoftWebWebview2Winforms] para APIs específicas de formulários Windows.  
*   Para obter mais informações sobre as APIs CoreWebView2, navegue até [.NET Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Problemas conhecidos**: a equipe do WebView está ciente de alguns problemas na pré-versão que estão sendo resolvidos em versões futuras.  
    > 
    > *   **Reconhecimento de DPI**: WebView2 para WPF atualmente não está ciente de DPI.  Ao inicializar o WebView2 em monitores DPI altos, há um problema conhecido em que o WebView inicialmente é inicializado como uma fração da janela até que a janela seja ressada.  
    > *   **Designer WPF**: O designer WPF não tem suporte no momento.  Adicione o controle WebView2 em seu aplicativo modificando diretamente o XAML apropriado em um editor de texto.  
    
## <a name="09488"></a>0.9.488  

[NuGet pacote][NuGetGallery0.9.488] \| Microsoft Edge versão 84.0.488.0.  

*   > [!IMPORTANT]
    > **Comunicado**: a partir do próximo Microsoft Edge versão 83, o Evergreen WebView não tem mais como alvo o canal do navegador Estável.  Em vez disso, ele se direciona a outro conjunto de binários, com a marca [Evergreen WebView2 Runtime][Webview2ConceptsDistributionEvergreenDistributionMode], que você pode instalar em cadeia por meio de um instalador que a equipe webView está desenvolvendo no momento.  Para obter mais informações, navegue até [App-Distribution][Webview2ConceptsDistribution].  
    
*   > [!IMPORTANT]
    > **Comunicado**: Seguindo em frente, a equipe webView lança dois pacotes: um pacote de pré-lançamento com APIs experimentais \(para você experimentar\) e um pacote de versão estável com APIs estáveis \(para sua confiança\).  Para saber mais sobre as diferenças, navegue até [Noções básicas sobre versões do navegador e WebView2][Webview2ConceptsVersioning].  
    
*   > [!IMPORTANT]
    > **Alteração de**quebra : para garantir que a API WebView2 se alinhe com as convenções de nomenis da API Windows, a equipe do WebView atualizou os nomes das interfaces a seguir.  
    > 
    > *   `CORE_WEBVIEW2_*` prefixo agora `COREWEBVIEW2_*` é .  
    > *   [GetCoreWebView2BrowserVersionInfo][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] agora [é GetAvailableCoreWebView2BrowserVersionString][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] agora está [get_BrowserVersionString][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring].  
    > *   [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] agora [é AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] agora [é RemoveHostObjectFromScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` agora `chrome.webview.hostObjects` é .  
    
*   > [!IMPORTANT]
    > **Alteração de Quebra**: os `AddRemoteObject` métodos proxy JS também são renomeados.  
    > 
    > *   `getLocal` agora `getLocalProperty` é .  
    > *   `setLocal` agora `setLocalProperty` é .  
    > *   `getRemote` agora `getHostProperty` é .  
    > *   `setRemote` agora `setHostProperty` é .  
    > *   `applyRemote` agora `applyHostFunction` é .  
    
*   > [!IMPORTANT]
    > **Alteração de Quebra**: Preterido [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] e substituído por [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   Evento [FrameNavigationCompleted][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted] adicionado.  Agora, quando um elemento conclui a navegação, um evento é executado e retorna o sucesso da navegação `iframe` e da ID de navegação.  
*   Adicionada [a interface ICoreWebView2EnvironmentOptions,][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] que pode ser usada para determinar a versão do Evergreen WebView2 Runtime direcionado pelo seu aplicativo.  
*   Foi [adicionada a configuração IsBuiltInErrorPageEnabled.][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]  Agora, você pode optar por ativar ou desativar a página da Web de erro interna para falha de navegação e processar a falha no processo.  
*   Injeção de objeto remoto atualizada para dar suporte a implementações do .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Evento [NewWindowRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] atualizado para lidar com solicitações de menus de contexto \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Lançou o primeiro pacote de pré-lançamento separado webView2 onde você pode acessar APIs de hospedagem visual.  A equipe do WebView [atualizou APISample][GithubMicrosoftedgeWebview2samplesMain] para incluir as novas APIs experimentais.  
    *   Adicionada [a interface ICoreWebView2ExperimentalCompositionController,][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] para se conectar a uma árvore de composição e fornecer entrada para o WebView.  
    *   [ICoreWebView2ExperimentalPointerInfo][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease], que contém todas as informações de `POINTER_INFO` um .  Esse objeto é passado para SendPointerInput para injetar entrada de ponteiro no WebView.  
    *   [ICoreWebView2ExperimentalCursorChangedEventHandler][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease], que informa ao aplicativo quando o cursor do mouse sobre o WebView deve ser alterado.  Quando o mouse está sobre uma caixa de texto no WebView, o cursor muda da seta para o seletor.  A propriedade no aplicativo informa o que o cursor do mouse deve ser no momento `cursor` `CompositionController` para o WebView.  
        
## <a name="09430"></a>0.9.430  

[NuGet pacote][NuGetGallery0.9.430] \| Microsoft Edge versão 82.0.430.0.  

O SDK WebView2 é a versão beta oficial do Win32 C++, que incorpora várias solicitações de recursos de comentários.  A equipe webView tenta limitar o número de versões com alterações de quebra.  À medida que a disponibilidade geral se aproxima, várias alterações significativas são incorporadas na versão Beta.  

*   > [!IMPORTANT]
    > **Alteração de**quebra : à medida que a versão final se aproxima, a equipe webView renomeou o prefixo para para a fim de garantir que `IWebView2WebView` a API WebView2 se alinhe com a convenção Windows de nomenis de `ICoreWebView2` API de Windows.  Além disso, para aproveitar o SDK WebView2 de estruturas da interface do usuário, a equipe webView separada em `ICoreWebView2` [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] e [ICoreWebView2Host][Webview2ReferenceWin32Icorewebview2hostViewWebview209430].  `ICoreWebView2Host` suporta resizing, showing-and-hiding, focusing, and other functionality related to windowing and composition.  O ICoreWebView2 oferece suporte a todas as outras funcionalidades do WebView2.  Para saber mais sobre como incorporar as alterações, navegue até a solicitação de [pull][GithubMicrosoftedgeWebview2samplesPr17] WebView2 no projeto [APISample][GithubMicrosoftedgeWebview2samplesMain] webView2.  
    
*   > [!IMPORTANT]
    > **Alteração de Quebra**: Divida [DocumentStateChanged][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] em três componentes:  [SourceChanged,][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged] [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]e [HistoryChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged].  Agora, quando a URL de origem altera `SourceChanged` o evento é executado.  Quando o estado do histórico é `HistoryChanged` alterado, o evento é executado.  O `ContentLoading` evento é executado antes do script inicial quando um novo documento está sendo carregado.  
    
*   Adicionado suporte à arquitetura ARM64.  
*   Adicionado suporte ao Painel de Entrada Suave \(SIP\) para dispositivos de tela touch.  
*   Adicionado suporte para Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 e Windows Server 2016.  
*   Foi [adicionado NotifyParentWindowPositionChanged][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] para que a barra de status seguisse a janela no modo de janela.  Além disso, implemente a alteração no modo sem janela para que os recursos de acessibilidade funcionem.  
*   A [configuração AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] foi adicionada para controlar globalmente se uma página da Web pode ser acessada por qualquer objeto remoto.  Por padrão, está ligado, para que objetos remotos adicionados `AreRemoteObjectsAllowed` por [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] sejam acessíveis a partir da página da Web.  Quando `AreRemoteObjectsAllowed` está desligado, os objetos não são acessíveis a partir da página da Web.  As alterações são aplicadas no próximo evento de navegação.  
*   Foi [adicionada a configuração IsZoomControlEnabled][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] para impedir que os usuários impactem o zoom do WebView usando `ctrl` + `+` e `ctrl` + `-` \(ou `ctrl` + roda do mouse\).  O zoom ainda pode ser definido usando [put_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] quando a configuração estiver desligada.  
*   Alterado ZoomFactor para aplicar apenas ao WebView atual.  As alterações de zoom no WebView atual não afetam outros WebViews que você navegueu usando o mesmo site de origem.  Para obter mais informações, navegue [até get_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor].  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Adicionado [SetBoundsAndZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor].  Agora, você pode definir o fator de zoom e os limites de um WebView ao mesmo tempo.  
*   Evento [WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] adicionado.  Para obter mais informações, navegue [até add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Adicionado suporte para o tipo de caixa de diálogo para eventos de caixa de diálogo `beforeunload` JavaScript e adicionado [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind] entrada de número.  
*   Foram [adicionados GetHeaders][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] a HttpRequestHeaders, [GetHeader][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] a HttpResponseHeaders e get_HasCurrentHeader [propriedade][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] httpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Alteração de Quebra**: Comportamento `DevToolsProtocolEventReceived` modificado.  Agora, você pode criar um [DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] para um evento específico do Protocolo DevTools e assinar/cancelar a inscrição para esse evento usando [add_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived].  
    
*   > [!IMPORTANT]
    > **Alteração de Alteração**: get_WebMessageAsString `WebMessageReceivedEventArgs` [][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] para um [método TryGetWebMessageAsString.][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]  
    
*   > [!IMPORTANT]
    > **Alteração de Alteração**: Método `AcceleratorKeyPressedEventArgs` [De manipular][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] alterado para uma [propriedade get_Handled][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled] de dados.  
    
## <a name="08355"></a>0.8.355  

[NuGet pacote][NuGetGallery0.8.355] \| Microsoft Edge versão 80.0.355.0.  

*   WebView2API Sample lançado, um guia abrangente do SDK WebView2.  Para obter mais informações, navegue até [API Sample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Adicionado suporte ao IME para todos os idiomas além do inglês \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Atualizou a superfície da API do `WebResourceRequested` evento em resposta a relatórios de bugs.  A especificação simultânea de um filtro e um evento na criação agora está preterida.  Para criar um evento solicitado por recurso web, use [add_WebResourceRequested][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] adicionar o evento e [AddWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] para adicionar um filtro.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] remove o filtro \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Alteração de Quebra**: Comportamento modificado em tela inteira.  Preterido [IsFullScreenAllowed][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated].  Agora, por padrão, se um elemento em um WebView \(como um vídeo\) estiver definido como tela inteira, ele preencherá os limites do WebView.  Use o [evento ContainsFullScreenElementChanged][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] [e][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement] o get_ContainsFullScreenElement para especificar como o aplicativo deve reencaminhar o WebView se um elemento quiser inserir o modo de tela inteira.  
    
## <a name="08314"></a>0.8.314  

[NuGet pacote][NuGetGallery0.8.314] \| Microsoft Edge versão 80.0.314.0.  

*   Adicionado suporte para Windows 7, Windows 8 e Windows 8.1.  
*   Adicionado Visual Studio e Visual Studio Code de depuração para WebView2.  Agora, depure seu script no WebView2 direto do seu IDE.  Para obter mais informações, navegue [até Como depurar ao desenvolver com controles WebView2][Webview2HowtoDebug].  
*   Adicionado para o script em execução no WebView2 para acessar um objeto IDispatch do componente Win32 do aplicativo e acessar as propriedades do objeto `Native Object Injection` IDispatch.  Para obter mais informações, navegue [até AddRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Evento `AcceleratorKeyPressed` adicionado.  Para obter mais informações, navegue [até add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Desligado o `Context Menus` .  Para obter mais informações, navegue [até put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Atualizado `DPI Awareness` .  Agora, o reconhecimento de DPI do WebView é o mesmo que o reconhecimento de DPI do aplicativo host.  
    
    > [!NOTE]
    > Se outro aplicativo híbrido for lançado com um Reconhecimento de DPI diferente do WebView original, o novo WebView não será lançado se for o mesmo `user data folder` \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Atualizado `Notification Change Behavior` para que o WebView2 rejeite automaticamente as solicitações de permissão de notificação solicitados pelo conteúdo da Web hospedado no WebView.  
    
## <a name="08270"></a>0.8.270  

[NuGet pacote][NuGetGallery0.8.270] \| Microsoft Edge versão 78.0.270.0.  

*   Evento `DocumentTitleChanged` adicionado para indicar a alteração de título do documento \([\#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Adicionado `GetWebView2BrowserVersionInfo` API \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Evento `NewWindowRequested` adicionado.  
*   Função `CreateWebView2EnvironmentWithDetails` atualizada para remover `releaseChannelPreference` .  Para obter mais informações sobre a `CreateWebView2EnvironmentWithDetails` função, navegue até [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  A substituição de variável de registro e ambiente ainda é suportada.  A preferência de canal padrão é usada, a menos que seja substituído.  
    Durante a pesquisa de canal, a equipe do WebView ignora qualquer versão de canal anterior que não seja compatível com o SDK WebView2.  
    A equipe do WebView seleciona o canal mais estável para garantir os comportamentos mais consistentes para o usuário final.  Ao testar com as versões canárias mais recentes, você deve criar um script para definir a variável de ambiente como `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` antes de iniciar o `1` aplicativo.  
*   Atualizou `CreateWebView2EnvironmentWithDetails` a função com lógica para selecionar quando não `userDataFolder` especificado.  Para obter mais informações sobre a `CreateWebView2EnvironmentWithDetails` função, navegue até [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Se você usou o local padrão anteriormente, quando você alterna para o novo SDK, o padrão é `userDataFolder` `userDataFolder` redefinido \(set to a new location in the host code directory\) and your state is also reset.  Se o processo de host não tiver permissão para gravar no diretório especificado, a `CreateWebView2EnvironmentWithDetails` função poderá falhar.  Você pode copiar os dados do antigo `user data folder` para o novo diretório.  
    
## <a name="08230"></a>0.8.230  

[NuGet pacote][NuGetGallery0.8.230] \| Microsoft Edge versão 77.0.230.0.  

*   Adicionada a API para interromper todas as buscas de recursos e navegação `Stop` pendentes \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Arquivo `.tlb` adicionado ao pacote NuGet \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Adicionados projetos .NET à lista do instalador no pacote de NuGet \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  
    
## <a name="08190"></a>0.8.190  

[NuGet pacote][NuGetGallery0.8.190] \| Microsoft Edge versão 77.0.190.0.  

*   Adicionado `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` ao controle se os usuários puderem abrir o DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Adicionado `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` ao controle se a barra de status for exibida \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Adicionado `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` para voltar e encaminhar pelo histórico de navegação.  
*   Adicionado tipos de cabeçalho HTTP \( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) para exibição e modificação de cabeçalhos HTTP no WebView.  
*   Adicionado suporte a WebView de 32 bits em máquinas de 64 bits \([\#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Adicionada a IDL do WebView ao SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Adicionado lib para dar suporte a `IID\_\*` objetos de ID da interface \([\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Adicionado incluem caminho, vinculação e autocópia de arquivos DLL para NuGet `TARGET` arquivo no SDK.  
*   Ligado solicitando `window.open()` no script.  
    
## <a name="08149"></a>0.8.149  

[NuGet pacote][NuGetGallery0.8.149] \| Microsoft Edge versão 76.0.149.0.  

Versão inicial de visualização do desenvolvedor.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Modo de distribuição evergreen - Distribuição de aplicativos usando WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Modo de distribuição de versão fixa - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Entenda o WebView2 Runtime e o instalador - Distribuição de aplicativos usando o webView2 | Microsoft Docs"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Políticas de grupo para WebView2 - Gerenciando aplicativos WebView2 | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Noções básicas sobre versões do navegador e webView2 | Microsoft Docs"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "APIs experimentais - Noções básicas sobre versões do navegador e webView2 | Microsoft Docs"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Correspondência de versões do Tempo de Execução do WebView2 - Entenda as versões do SDK webView2 | Microsoft Docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Como começar com o WebView2 Windows aplicativos forms | Microsoft Docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Como começar com WebView2 no WPF | Microsoft Docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Como depurar ao desenvolver com controles WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental2?view=webview2-1.0.865-prerelease&preserve-view=true#add_downloadstarting  "add_DownloadStarting - interface ICoreWebView2Experimental2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment3?view=webview2-1.0.865-prerelease&preserve-view=true#updateruntime  "UpdateRuntime - interface ICoreWebView2ExperimentalEnvironment3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalframe?view=webview2-1.0.865-prerelease&preserve-view=true#addhostobjecttoscriptwithorigins  "AddHostObjectToScriptWithOrigins - interface ICoreWebView2ExperimentalFrame | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings4?view=webview2-1.0.865-prerelease&preserve-view=true#ispinchzoomenabled  "IsPinchZoomEnabled - interface ICoreWebView2ExperimentalSettings4 | Microsoft Docs" 

[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings2?view=webview2-1.0.824&preserve-view=true#get_arebrowseracceleratorkeysenabled "get_AreBrowserAcceleratorKeyPressed - interface ICoreWebView2ExperimentalSettings | Microsoft Docs" 

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - interface ICoreWebView2_2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping - interface ICoreWebView2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend - interface ICoreWebview2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled - interface ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "interface ICoreWebView2CompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor - interface ICoreWebView2Controller2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived - interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived - interface ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest - interface ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interface ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount - interface ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments - interface ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo - interface ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString - interface ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged - interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode - interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale - interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges - interface ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled - interface ICoreWebView2ExperimentalEnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures - interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalPointerInfo | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent - interface ICoreWebView2ExperimentalSettings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded - interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived - interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager - interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment - interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest - interface ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent - interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interface ICoreWebView2ExperimentalWindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor - interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged - interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor - interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor - interface ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader - interface ICoreWebView2HttpHeadersCollectionIterator | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders - interface ICoreWebView2HttpRequestHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader - interface ICoreWebView2HttpResponseHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated interface ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures - interface ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled - interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed - interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled "get_IsBuiltInErrorPageEnabled - interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed - interface ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript - interface ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString - interface ICoreWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invocar - interface ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interface ICoreWebView2WindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle - interface IWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interface IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled - interface IWebView2Settings2 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated - interface IWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString - interface IWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed - interface IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject - interface IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested - interface IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter - interface IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement - interface IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter - interface IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged - interface IWebView2WebView | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge - Políticas | Microsoft Docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2 - Políticas | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft.Web.WebView2.Core | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Classe CoreWebView2 (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Classe CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Método CoreWebView2Environment.CompareBrowserVersions(String, String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Método CoreWebView2Environment.GetAvailableBrowserVersionString(String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Classe CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Classe CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Evento CoreWebView2.NewWindowRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Evento CoreWebView2.PermissionRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Evento CoreWebView2.ScriptDialogOpening (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Evento CoreWebView2.WebResourceRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Classe CoreWebView2InitializationCompletedEventArgs | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Classe CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Classe Webview2.Source (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Método WebView2.BuildWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Método WebView2.DestroyWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Classe CancelEventArgs (System.ComponentModel) | Microsoft Docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Classe EventArgs (System) | Microsoft Docs"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Assemblies com nome | Microsoft Docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Microsoft Defender Application Guard (Windows 10) - Windows segurança | Microsoft Docs"  
[WindowsWin32ApiWinuserSetWindowDisplayAffinity]: /windows/win32/api/winuser/nf-winuser-setwindowdisplayaffinity "Função SetWindowDisplayAffinity (winuser.h) - Aplicativos Win32 | Microsoft Docs"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Repo de comunicado para o MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Exemplo de API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Exemplos de WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2WpfBrowser "WebView2WpfBrowser - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Mover projeto para usar o SDK 0.9.430 mais recente do WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Problema 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Problema 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Repo de comentários do MicrosoftEdge/WebViewFeedback Issue 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Repo de comentários do MicrosoftEdge/WebViewFeedback Issue 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Repo de comentários do MicrosoftEdge/WebViewFeedback Problema 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue506]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/506 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 506"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue568]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/568 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 568"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue604]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/604 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 604"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue669]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/669 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 669"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue851]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/851 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 851"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 878"  
[GithubMicrosoftedgeWebviewfeedbackIssue1120]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1120 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 1120"
[GithubMicrosoftedgeWebviewfeedbackIssue940]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/940 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 940"
[GithubMicrosoftedgeWebviewfeedbackIssue841]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/841 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 841"
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 210"
[GithubMicrosoftedgeWebviewfeedbackIssue338]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/338 "Feedback repo for MicrosoftEdge/WebViewFeedback Issue 338"
[GithubMicrosoftedgeWebviewfeedbackIssue589]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/589 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 589"
[GithubMicrosoftedgeWebviewfeedbackIssue933]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/933 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 933"
[GithubMicrosoftedgeWebviewfeedbackIssue946]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/946 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 946"
[GithubMicrosoftedgeWebviewfeedbackIssue1011]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1011 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 1011"
[GithubMicrosoftedgeWebviewfeedbackIssue1050]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1050 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 1050"
[GithubMicrosoftedgeWebviewfeedbackIssue996]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/996 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 996"
[GithubMicrosoftedgeWebviewfeedbackIssue850]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/850 "Repo de comentários para o MicrosoftEdge/WebViewFeedback Issue 850"

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Anunciando a disponibilidade geral para Microsoft Edge WebView2 para o .NET e o Método de Distribuição Fixa | Blog .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Edge Desenvolvedor"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "NuGet Galeria | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "NuGet Galeria | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "NuGet Galeria | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "NuGet Galeria | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "NuGet Galeria | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "NuGet Galeria | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "NuGet Galeria | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "NuGet Galeria | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "NuGet Galeria | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "NuGet Galeria | Pré-lançamento do Microsoft.Web.WebView2 v0.9.515"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "NuGet Galeria | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "NuGet Galeria | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "NuGet Galeria | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "NuGet Galeria | Pré-lançamento do Microsoft.Web.WebView2 v0.9.628"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "NuGet Galeria | Microsoft.Web.WebView2 v1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "NuGet Galeria | Microsoft.Web.WebView2 v1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "NuGet Galeria | Microsoft.Web.WebView2 v1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "NuGet Galeria | Pré-lançamento do Microsoft.Web.WebView2 v1.0.674"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "NuGet Galeria | Microsoft.Web.WebView2 v1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "NuGet Galeria | Pré-lançamento do Microsoft.Web.WebView2 v1.0.721"  
[NuGetGallery1.0.774.44]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.774.44 "NuGet Galeria | Microsoft.Web.WebView2 v1.0.774.44"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "NuGet Galeria | Pré-lançamento do Microsoft.Web.WebView2 v1.0.790"  
[NuGetGallery1.0.818.41]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.818.41 "NuGet Galeria | Microsoft.Web.WebView2 v1.0.818.41"  
[NuGetGallery1.0.824-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.824-prerelease "NuGet Galeria | Pré-lançamento do Microsoft.Web.WebView2 v1.0.824"  
[NuGetGallery1.0.865-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.865-prerelease "NuGet Galeria | Pré-lançamento do Microsoft.Web.WebView2 v1.0.865"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Anunciando Microsoft Edge disponibilidade geral do WebView2 | Microsoft Edge Blog"  
