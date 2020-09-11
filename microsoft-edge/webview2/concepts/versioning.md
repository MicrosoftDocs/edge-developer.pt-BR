---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 3ce1f0653a14d92571f1365cbfebc8bb2215ecbe
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010674"
---
# Entender as versões do SDK do WebView2  

O WebView2 depende do Microsoft Edge para funcionar.  Cada SDK do WebView2 requer a instalação de uma versão mínima do navegador.  A versão mínima é refletida na versão do pacote do SDK.  Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o Microsoft Edge com um número de compilação de 488 ou posterior.  A versão do navegador também é especificada nas [notas de versão][Releasenotes]do WebView2.  Para obter mais informações sobre a versão mais recente do navegador Microsoft Edge, navegue até [canais do navegador][DeployedgeChannels].  

> [!NOTE]
> O WebView2 está atualmente em visualização.  Enquanto a equipe da WebView se empenha para garantir a compatibilidade com versões anteriores entre as versões e os SDKs do navegador, não é garantido porque versões mais recentes do navegador podem não dar suporte a versões anteriores do SDK.  Se houver alterações significativas entre versões e SDKs do navegador, as alterações serão especificadas nas [notas de versão][Releasenotes].  

No futuro, a equipe da WebView planeja alterar o modelo de distribuição para aplicativos do WebView2.  Para obter mais informações, navegue até o [modo de distribuição do verde][DistributionEvergreenMode].  

## Liberar e lançar pacote  

Na visualização, o pacote de lançamento contém o seguinte.  

*   [APIs C/C++ do Win32][ReferenceWin3209622]: APIs no SDK que devem permanecer iguais no ga.  

Na visualização, o pacote de pré-lançamento contém os componentes a seguir.  

*   APIs .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]e [núcleo][ReferenceDotnet09628]  
*   APIs experimentais.  Para obter mais informações, consulte a seção [APIs experimentais](#experimental-apis) .  

## APIs experimentais  

A equipe da WebView está testando APIs experimentais que podem representar funcionalidades futuras.  As APIs experimentais são marcadas como `experimental` no SDK.  APIs experimentais podem ser entregues como APIs totalmente estáveis no pacote de lançamento.  Você deve esperar que todas as APIs experimentais sejam alteradas antes do lançamento.  Avalie as APIs experimentais e compartilhe comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].  

> [!CAUTION]
> Evite usar as APIs experimentais em aplicativos de produção.  

## Correspondentes às versões do tempo de execução do WebView2  

Ao escrever um aplicativo do WebView2 usando uma versão específica do SDK, os usuários do seu aplicativo podem executá-lo com várias versões compatíveis do tempo de execução do WebView2.  No futuro, uma versão compatível mais recente do WebView2 Runtime contém todas as APIs não experimentais de uma versão de tempo de execução do WebView2 compatível mais antiga, além de novas APIs não experimentais adicionais.  

*   Os desenvolvedores de **C/C++ Win32** , ao usar `QueryInterface` para obter uma nova interface, devem verificar um valor de retorno de `E_NOINTERFACE` , o que pode indicar que o tempo de execução do WebView2 é mais antigo e não dá suporte a essa interface específica.  
*   Os desenvolvedores **.net e WinUI** devem verificar uma `No such interface supported` exceção ao usar métodos, propriedades e eventos adicionados em SDKs posteriores, que podem ocorrer quando o tempo de execução do WebView2 é mais antigo e não dá suporte a essas APIs específicas.  

Se uma API estiver indisponível, considere a possibilidade de desabilitar o recurso associado, se possível, ou informando ao usuário final que ele precisa atualizar a versão do WebView2 Runtime.  

APIs experimentais podem ser introduzidas, modificadas e removidas do SDK para o SDK.  Ao tentar usar uma API experimental que não está disponível no tempo de execução do WebView2, você pode observar o comportamento descrito anteriormente descrito.  

## Mapa  

Após o WebView2 atingir um estado de generally available, o pacote de lançamento contém todas as APIs de C/C++ e .NET do Win32 com suporte estável.  O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos seus comentários e ideias compartilhadas.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribuição em verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ReferenceDotnet09628]: ../reference/dotnet/0-9-628-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWin3209622]: ../reference/win32/0-9-622-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
