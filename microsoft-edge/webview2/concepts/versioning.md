---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 059bbeb34f372af0cef944e484599c0b50543cc9
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844422"
---
# Entender as versões do SDK do WebView2  

O WebView2 depende do Microsoft Edge para funcionar.  Cada SDK do WebView2 requer a instalação de uma versão mínima do navegador.  A versão mínima é refletida na versão do pacote do SDK.  Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o Microsoft Edge com um número de compilação de 488 ou posterior.  A versão do navegador também é especificada nas [notas de versão][Releasenotes]do WebView2.  Para obter mais informações sobre as versões mais recentes do navegador, consulte [canais do navegador][DeployedgeChannels].  

> [!NOTE]
> O WebView2 está atualmente em visualização.  Enquanto a equipe da WebView se empenha para garantir a compatibilidade com versões anteriores entre as versões e os SDKs do navegador, não é garantido porque as versões mais recentes do navegador podem não dar suporte a versões mais antigas do SDK.  Se houver alterações significativas entre versões e SDKs do navegador, a equipe da WebView especificará as alterações nas [notas de versão][Releasenotes].  

No futuro, a equipe da WebView planeja alterar o modelo de distribuição para aplicativos do WebView2.  Para obter mais informações, consulte ver o [modo de distribuição do verde][DistributionEvergreenMode].  
 
## Lançamento e pacote de pré-lançamento  

Na visualização, o pacote de lançamento contém o seguinte.  

*   [APIs C/C++ do Win32][ReferenceWin3209538]: APIs no SDK que devem permanecer iguais no ga. 

Na visualização, o pacote de pré-lançamento contém os componentes a seguir.  

*   APIs .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]e [núcleo][ReferenceDotnet09538]
*   APIs experimentais.  Para obter mais informações, consulte a seção [APIs experimentais](#experimental-apis) .  

### APIs experimentais  

A equipe da WebView está testando APIs que representam funcionalidades futuras nomeadas APIs experimentais.  As APIs experimentais são marcadas como `experimental` no SDK.  Algumas APIs experimentais podem ser entregues como APIs totalmente estáveis no pacote de lançamento.  Você deve esperar que todas as APIs experimentais sejam alteradas antes do lançamento.  Avalie as APIs experimentais e compartilhe comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Evite usar as APIs experimentais em aplicativos de produção.  

### Mapa  

Após o WebView2 atingir um estado de generally available, o pacote de lançamento contém todas as APIs de C/C++ e .NET do Win32 com suporte estável.  O pacote de pré-lançamento contém APIs experimentais sujeitas a alterações com base nos comentários do desenvolvedor e em ideias compartilhadas.  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Modo de distribuição em verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Referência (WebView2) | Documentos da Microsoft"  
[Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
