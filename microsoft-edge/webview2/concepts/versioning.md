---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/18/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 132ccab0f9f378eedd8c83a7404c350161556f2e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182392"
---
# Entender as versões do SDK do WebView2

As novas versões do SDK do WebView2 são fornecidas na mesma cadência geral do navegador Microsoft Edge \ (Chromium \), que é aproximadamente a cada seis semanas.  

## Liberar e lançar pacote  

O pacote NuGet WebView2 contém um pacote de pré-lançamento e de pré-lançamento.  

O pacote de versão é compatível com o redirecionamento e contém as [APIs C/C++ do Win32][ReferenceWin32].  APIs neste SDK são totalmente suportadas.  

O pacote de pré-lançamento é um superconjunto do pacote de versão com os componentes adicionais listados abaixo.  

*   APIs .NET: [WPF][DotnetMicrosoftWebWebview2WpfNamespace], [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]e [núcleo][DotnetMicrosoftWebWebview2CoreNamespace]  
*   APIs experimentais: para obter mais informações, navegue até a seção [APIs experimentais](#experimental-apis) .  

### Mapa  

O pacote de lançamento contém todas as APIs C/C++ de Win32 compatíveis e estáveis.  No futuro, o pacote de lançamento conterá todas as APIs do .NET compatíveis e estáveis, quando elas forem disponibilizadas de forma geral.  O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos seus comentários. 

## APIs experimentais  

A equipe da WebView está procurando comentários sobre APIs experimentais que podem ser incluídas em versões futuras.  As APIs experimentais são marcadas como `experimental` no SDK.  Você pode avaliar as APIs experimentadas e compartilhar comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> APIs experimentais podem ser introduzidas, modificadas e removidas do SDK para o SDK.  Evite usar as APIs experimentais em aplicativos de produção.  

> [!NOTE]
> APIs experimentais podem não estar disponíveis na versão instalada do tempo de execução do WebView2.  

## Correspondentes às versões do tempo de execução do WebView2  
Aplicativos WebView2 exigem que os usuários instalem um [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2]. O tempo de execução do WebView2 é atualizado automaticamente para a versão mais recente que está disponível. Em alguns cenários, os usuários podem precisar parar as atualizações automáticas do tempo de execução do WebView2, o que pode causar problemas de compatibilidade do aplicativo.

Se as atualizações do tempo de execução do WebView2 forem interrompidas, verifique se você entendeu a versão mínima do [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2] exigida pelo seu aplicativo. Considere os dois itens a seguir:  

1. A versão mínima necessária do SDK, que pode ser encontrada nas [notas de versão][Releasenotes] do WebView2 abaixo da **versão mínima do tempo de execução do WebView2**. Por exemplo, para o SDK versão [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222), você deve instalar o [tempo de execução do WebView2][MicrosoftDeveloperEdgeWebview2] ou um [canal do Microsoft Edge não estável][MicrosoftedgeinsiderDownload] com um número de compilação de **86.0.616.0** ou posterior. A versão mínima exigida pelo SDK será alterada apenas quando houver uma alteração significativa na plataforma da Web.

2. A versão mínima necessária do pacote NuGet que é necessário para dar suporte às interfaces e APIs usadas em seu aplicativo. Novas interfaces e APIs são adicionadas periodicamente ao WebView2. APIs e interfaces incluídas em um SDK exigem versões diferentes do tempo de execução do WebView2, porque elas foram adicionadas ao SDK em momentos diferentes.  A versão necessária do tempo de execução do WebView2 corresponde ao número da compilação, o terceiro número da versão do SDK na qual a API foi introduzida pela primeira vez. Por exemplo, uma nova API ou interface adicionada ao SDK versão [1.0.622.22](https://docs.microsoft.com/microsoft-edge/webview2/releasenotes#1062222) precisará da versão do WebView2 Runtime: 86,0. **622**. 0. Uma API ou interface adicionada em uma versão SDK subsequente exige o tempo de execução WebView2 que tem o mesmo número de versão do SDK. Você pode determinar se a versão do tempo de execução do WebView2 dá suporte a uma interface ou API [programaticamente](#determine-webview2-runtime-requirement).

> [!IMPORTANT]
> Ao desenvolver [aplicativos do WebView2](distribution.md#evergreen-distribution-mode)para o meio do tempo de execução, teste regularmente o aplicativo nas versões mais recentes do tempo de execução do WebView2 e dos navegadores não estáveis do Microsoft Edge.  Como a plataforma da Web está em constante evolução, o teste regular é a melhor maneira de garantir que seu aplicativo seja executado conforme o esperado.  

### Determinar requisito de tempo de execução do WebView2

Dependendo de qual SDK você usa, considere os seguintes itens: 

*   **Win32 C/C++**.  Ao usar `QueryInterface` para obter uma nova interface, verifique se há um valor de retorno `E_NOINTERFACE` .  Esse valor pode indicar que o tempo de execução do WebView2 é uma versão anterior e não dá suporte a essa interface. Navegue até o exemplo WebView2API para obter um [exemplo](https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622) de como isso funciona.
*   **.Net e WinUI**.  Verifique se há uma `No such interface supported` exceção ao usar métodos, propriedades e eventos que foram adicionados a SDKs mais recentes.  Essa exceção pode ocorrer quando o tempo de execução do WebView2 é uma versão anterior e não é compatível com essas APIs.  

Se uma API estiver indisponível, considere remover o recurso associado ou informar aos usuários que eles precisam atualizar a versão do tempo de execução do WebView2.  



 

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->  

[Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Namespace Microsoft. Web. WebView2. Core | Documentos da Microsoft"  
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Namespace Microsoft. Web. WebView2. WPF | Documentos da Microsoft"  
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Namespace Microsoft. Web. WebView2. WinForms | Documentos da Microsoft"  
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Referência de C++ do WebView2 Win32 | Documentos da Microsoft"  

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Desenvolvedor da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Baixar canais do Microsoft Edge Insider"  
