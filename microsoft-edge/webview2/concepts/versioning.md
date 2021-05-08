---
description: Modelos de versão usados para Microsoft Edge WebView2
title: Compreender versões do SDK webView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 18ae2b8feb9310798f78e67cbb767d0642d83d24
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535710"
---
# <a name="understand-webview2-sdk-versions"></a>Compreender versões do SDK webView2  

As novas versões do SDK WebView2 são enviadas na mesma cadência geral do navegador Microsoft Edge \(Chromium\), que é aproximadamente a cada seis semanas.  

## <a name="release-and-prerelease-package"></a>Pacote de lançamento e pré-lançamento  

O pacote de NuGet WebView2 contém um pacote de versão e pré-lançamento.  

O **pacote de versão** é compatível com encaminhamento e contém os seguintes componentes.  

*   [Win32 C/C++ APIs][ReferenceWin32]
*   APIs .NET:  [WPF,][DotnetMicrosoftWebWebview2WpfNamespace] [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]e [Core][DotnetMicrosoftWebWebview2CoreNamespace].  
    
As APIs no SDK são totalmente suportadas.  

O **pacote de pré-lançamento** é um superconjunto do pacote de lançamento com [APIs Experimentais](#experimental-apis).  Evite usar o SDK de pré-lançamento para criar aplicativos de produção.  

### <a name="roadmap"></a>Mapa  

O pacote de versão contém todas as APIs win32 C/C++ e .NET estáveis.  O pacote de pré-lançamento contém APIs experimentais que estão sujeitas a alterações com base em seus comentários.  

## <a name="experimental-apis"></a>APIs experimentais  

A equipe do WebView está procurando comentários sobre APIs experimentais que podem ser incluídas em versões futuras.  As APIs experimentais são `experimental` marcadas como no SDK.  Para ajudá-lo a avaliar as APIs Experimentais e compartilhar seus comentários, navegue até o [repo de comentários do WebView.][GithubMicrosoftedgeWebviewfeedback]  

> [!CAUTION]
> APIs experimentais podem ser introduzidas, modificadas e removidas do SDK para o SDK.  Evite usar as APIs experimentais em aplicativos de produção.  

> [!NOTE]
> As APIs experimentais podem não estar disponíveis na versão instalada do Tempo de Execução do WebView2.  

## <a name="matching-webview2-runtime-versions"></a>Correspondência de versões do Tempo de Execução do WebView2  
Os aplicativos WebView2 exigem que os usuários instalem um [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2].  O WebView2 Runtime é atualizado automaticamente para a versão mais recente disponível.  Em alguns cenários, os usuários podem querer interromper atualizações automáticas do WebView2 Runtime, o que pode causar problemas de compatibilidade de aplicativos.  

Se as atualizações do Tempo de Execução do WebView2 são interrompidas, certifique-se de entender a versão mínima do Tempo de Execução [do WebView2][MicrosoftDeveloperEdgeWebview2] exigido pelo seu aplicativo.  Considere os dois itens a seguir:  

1.  A versão mínima necessária do SDK para carregar com êxito uma instância webview2 é encontrada nas Notas de Versão do [WebView2][Webview2ReleaseNotes] em Versão mínima Microsoft Edge para **carregar**.  A versão mínima para carregar necessária pelo SDK só muda quando ocorre uma alteração significativa na plataforma Web.  Por exemplo, para o SDK versão [1.0.622.22][Webview2ReleaseNotes1062222], você deve instalar o [WebView2 Runtime][MicrosoftDeveloperEdgeWebview2] ou um canal Microsoft Edge não estável com um número de com build de ou mais [recente.][MicrosoftedgeinsiderDownload] `86.0.616.0`   
1.  A versão mínima necessária do pacote NuGet necessário para dar suporte às interfaces e APIs [][Webview2ReleaseNotes] em seu aplicativo é encontrada nas Notas de Versão do WebView2 em Compatibilidade **completa da API**.  Novas interfaces e APIs são adicionadas periodicamente ao WebView2.  APIs e interfaces agrupadas em um SDK exigem versões diferentes do Tempo de Execução do WebView2, pois APIs e interface são adicionadas ao SDK em momentos diferentes.  A versão de Tempo de Execução do WebView2 necessária corresponde ao número de com build, o terceiro número, da versão SDK em que a API foi introduzida pela primeira vez.  Por exemplo, uma nova API ou interface adicionada ao SDK versão [1.0.622.22][Webview2ReleaseNotes1062222] requer a versão do Tempo de Execução do WebView2 ou `86.0.622.0` mais recente.  Uma API ou interface adicionada em uma versão SDK posterior requer um Tempo de Execução webView2 que tenha o mesmo número de versão do SDK.  Para ajudá-lo a determinar se a versão do Tempo de Execução do WebView2 dá suporte a uma interface ou API, navegue até [Determine WebView2 Runtime requirement](#determine-webview2-runtime-requirement).  
    
> [!IMPORTANT]
> Ao desenvolver [aplicativos Evergreen WebView2,][Webview2ConceptsDistributionEvergreenDistributionMode]teste regularmente seu aplicativo em relação às versões mais recentes do WebView2 Runtime e canais não estáveis Microsoft Edge.  Como a plataforma Web está em constante evolução, o teste regular é a melhor maneira de garantir que seu aplicativo execute conforme o esperado.  

### <a name="determine-webview2-runtime-requirement"></a>Determinar o requisito de tempo de execução do WebView2  

Dependendo do SDK usado, considere os seguintes itens:  

*   **Win32 C/C++**.  Ao usar `QueryInterface` para obter uma nova interface, verifique um valor de retorno de `E_NOINTERFACE` .  O valor pode indicar que o WebView2 Runtime é uma versão anterior e não dá suporte a essa interface.  Para um exemplo de como ele funciona, navegue até [a Linha 622 - AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622].  
*   **.NET e WinUI**.  Verifique se há uma exceção ao usar métodos, propriedades e eventos que `No such interface supported` foram adicionados a SDKs mais recentes.  A exceção pode ocorrer quando o Tempo de Execução do WebView2 for uma versão anterior e não suportar as APIs.  
    
Se uma API não estiver disponível, considere remover o recurso associado ou informar aos usuários que uma atualização para o Tempo de Execução do WebView2 é necessária.  

<!--
## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  
1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  
    -->  

<!--links -->  

[Webview2ConceptsDistributionEvergreenDistributionMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribuição evergreen - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[Webview2ReleaseNotes]: ../release-notes.md "Notas de versão do SDK WebView2 | Microsoft Docs"  
[Webview2ReleaseNotes1062222]: ../release-notes.md#1062222 "1.0.622.22 - Notas de versão para | Microsoft Docs"   

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos Microsoft Edge canais | Microsoft Docs"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft.Web.WebView2.Core | Microsoft Docs"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++ Reference | Microsoft Docs"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Desenvolvedor da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCppL622]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "Linha 622 - AppWindow.cpp - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar o Microsoft Edge Insider Channels"  
