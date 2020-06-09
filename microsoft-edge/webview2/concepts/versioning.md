---
description: Modelos de controle de versão usados para o Microsoft Edge WebView2
title: Controle de versão do Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: cc924a146057a3c8c578ccea187e1dd63dedcbe6
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697214"
---
# Noções básicas sobre versões do navegador e WebView2  

O WebView2 depende do Microsoft Edge para funcionar.  Cada SDK do WebView2 requer a instalação de uma versão mínima do navegador.  Esta versão do navegador está especificada nas nossas [notas de lançamento][Webview2Releasenotes].  Você pode ver a versão mínima refletida na versão do pacote do SDK.  Por exemplo, se você usar o `SDK package version 0.9.488` , será necessário instalar o Microsoft Edge com um número de compilação de 488 ou posterior.  Para obter mais informações sobre as versões mais recentes do navegador, consulte [canais do navegador][DeployedgeChannels].  

> [!NOTE]
> O WebView2 está atualmente em visualização.  Enquanto a equipe do Microsoft Edge WebView se empenha para garantir a compatibilidade com versões anteriores entre as versões e os SDKs do navegador, não é garantido que algumas versões mais recentes do navegador possam não dar suporte a versões mais antigas do SDK.  Se houver alterações significativas entre versões e SDKs do navegador, a equipe do Microsoft Edge WebView indicará as alterações nas [notas de versão][Webview2Releasenotes].  

No futuro, a equipe do Microsoft Edge WebView planeja alterar o modelo de distribuição.  A equipe do Microsoft Edge WebView planeja remover a dependência direta do navegador Microsoft Edge da WebView2.  Para saber mais, consulte [tempo de execução do WebView2][Webview2IndexEdgeRuntime] na seção [distribuição][Webview2Distibution] .  

## APIs experimentais  

Embora o WebView2 seja uma visualização, espera-se que as APIs no SDK permaneçam as mesmas no GA.  Há [APIs experimentais][Webview2ReferenceWin3209538Experimental] incluídas no SDK.  Avalie as APIs experimentais e envie seus comentários usando o [repositório de comentários da WebView][GithubMicrosoftedgeWebviewfeedback].  

### Mapa  

Depois que o WebView2 atinge um estado de general General estável e lançamos o SDK do 1.0.0, a equipe do Microsoft Edge WebView planeja mover todas as APIs experimentais para um pacote de pré-lançamento.  O pacote de pré-lançamento continua a permitir comentários e obter informações sobre os recursos mais recentes, enquanto a versão de lançamento estável mantém a compatibilidade com versões anteriores.  

<!--links -->

[Webview2Distibution]: ./distribution.md "Distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2 Runtime-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[Webview2ReferenceWin3209538Experimental]: ../reference/win32/0-9-538-reference-webview2.md#experimental "Experimental-Reference (WebView2) | Documentos da Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de versão do WebView2 SDK | Documentos da Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Visão geral dos canais Microsoft Edge | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
