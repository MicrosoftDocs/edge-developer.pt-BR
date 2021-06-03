---
description: Entender como gerenciar aplicativos WebView2
title: Gerenciando aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda, empresa, política de grupo, capacidade de gerenciamento
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057856"
---
# Gerenciando aplicativos WebView2  

[WebView2][WebView2Landing] é um componente que os desenvolvedores usam para criar seus aplicativos, e os desenvolvedores podem implantar um [Evergreen WebView2 Runtime][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] de atualização automática no dispositivo do usuário para acionar seus aplicativos.  Este documento discute como os administradores de IT podem gerenciar aplicativos WebView2 e Tempo de Execução.  Comentários de administradores de IT e desenvolvedores são bem-vindos no [repo comentários do WebView2][GithubMicrosoftedgeWebviewfeddback].  

## Políticas de grupo para WebView2  

Os administradores de IT podem usar objetos de política de grupo \(GPO\) para definir configurações de política para WebView2.  O conjunto de políticas a seguir é/não se aplica a WebView2,  

*   [Microsoft Edge - As políticas][EdgeUpdatePolicies] de atualização estão disponíveis para os administradores de IT gerenciarem os aspectos de instalação e atualização do Tempo de Execução do WebView2.  O Microsoft Edge e o Tempo de Execução do WebView2 são atualizados usando o mesmo mecanismo de atualização.  A menos que uma política, como , seja específica do canal, ela se aplica ao navegador e ao Tempo de Execução `Update` do WebView2.  Por exemplo, permite que os administradores de IT deem um tempo durante cada dia para suprimir a atualização automática para o navegador e o Tempo de Execução `UpdateSuppressed` do WebView2.  Isso permite que os administradores de IT configurem preferências e proxies uma vez para o navegador e o Tempo de Execução do WebView2 controlar sua largura de banda/tráfego de rede ou para outras finalidades.  Os administradores de IT podem [seguir Microsoft Edge guia da][ConfigureMicrosoftEdge] Microsoft Edge - Atualizar políticas.  
*   [Microsoft Edge - As políticas do navegador][EdgeBrowserPolicies] não se aplicam a aplicativos WebView2.  Isso é por design porque os aplicativos e navegadores têm casos de uso diferentes, e os administradores de IT podem não estar cientes de quais aplicativos usam WebView2.  A aplicação de políticas de navegador no WebView2 pode ter consequências não intencionais.  Por exemplo, os administradores de IT podem bloquear o JavaScript no navegador e todos os aplicativos WebView2 usando JavaScript estão quebrados.  
*   \(Em breve\) Políticas específicas do WebView2 – WebView2 exporá um pequeno conjunto adicional de políticas de grupo em casos em que o gerenciamento do WebView2 faz sentido diretamente.  Recomendamos que os desenvolvedores de aplicativos implementem suas próprias políticas de grupo para gerenciar o uso do WebView2, pois é mais simples para os administradores de IT gerenciar o aplicativo em vez de WebView2 diretamente.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Entenda o WebView2 Runtime e o instalador (Visualização) - Distribuição de aplicativos usando o webView2 | Microsoft Docs"  

[WebView2Landing]: ../index.md "Introdução ao Microsoft Edge WebView2 (Visualização) | Microsoft Docs"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge - Atualizar políticas | Microsoft Docs"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge - Políticas de navegador | Microsoft Docs"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurar Microsoft Edge configurações de política no Windows | Microsoft Docs"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
