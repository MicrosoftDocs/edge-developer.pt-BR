---
description: Entender como gerenciar aplicativos do WebView2
title: Gerenciando aplicativos WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, HTML de borda, empresa, política de grupo, gerenciabilidade
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057856"
---
# Gerenciando aplicativos WebView2  

O [WebView2][WebView2Landing] é um componente que os desenvolvedores usam para criar seus aplicativos, e os desenvolvedores podem implantar um [tempo de execução do WebView2 de autoatualização do tempo de execução do][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] no dispositivo do usuário para poder ligá-los.  Este documento discute como os administradores de ti podem gerenciar aplicativos e tempo de execução do WebView2.  Comentários de administradores de ti e desenvolvedores são bem-vindos no [repositório de comentários do WebView2][GithubMicrosoftedgeWebviewfeddback].  

## Políticas de grupo para WebView2  

Os administradores de ti podem usar objetos de política de grupo \ (GPO \) para definir configurações de política para WebView2.  O conjunto de políticas a seguir é/não se aplica a WebView2,  

*   [Microsoft Edge-as políticas de atualização][EdgeUpdatePolicies] estão disponíveis para administradores de ti gerenciar os aspectos de instalação e atualização do tempo de execução do WebView2.  O navegador Microsoft Edge e o tempo de execução do WebView2 são atualizados usando o mesmo mecanismo de atualização.  A menos que uma política, por exemplo `Update` , seja específica do canal, ela se aplica ao navegador e ao tempo de execução do WebView2.  Por exemplo, `UpdateSuppressed` permite que os administradores de ti definam o tempo durante cada dia para suprimir a atualização automática para o navegador e o tempo de execução do WebView2.  Isso permite que os administradores de ti configurem preferências e proxies uma vez para o navegador e o tempo de execução do WebView2 para controlar a largura de banda/o tráfego da rede ou para outras finalidades.  Os administradores de ti podem seguir [o guia do Microsoft Edge][ConfigureMicrosoftEdge] para configurar as políticas de atualização do Microsoft Edge.  
*   [Microsoft Edge-as políticas do navegador][EdgeBrowserPolicies] não se aplicam a aplicativos do WebView2.  Isso ocorre por design porque aplicativos e navegadores têm casos de uso diferentes, e administradores de ti podem não estar cientes do que os aplicativos usam o WebView2.  A aplicação de políticas de navegador no WebView2 pode ter conseqüências indesejadas.  Por exemplo, os administradores de ti podem bloquear JavaScript no navegador e todos os aplicativos do WebView2 que usam JavaScript são desfeitos.  
*   \ (Em breve \) WebView2 políticas específicas – o WebView2 irá expor um pequeno conjunto adicional de políticas de grupo nos casos em que o gerenciamento do WebView2 faz sentido diretamente.  Recomendamos que os desenvolvedores de aplicativos implementem suas próprias políticas de grupo para gerenciar o uso do WebView2, pois é mais simples para administradores de ti gerenciar o aplicativo, em vez de WebView2 diretamente.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Compreenda o tempo de execução do WebView2 e o instalador (visualização)-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  

[WebView2Landing]: ../index.md "Introdução ao Microsoft Edge WebView2 (visualização) | Documentos da Microsoft"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge-atualizar políticas | Documentos da Microsoft"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge-políticas do navegador | Documentos da Microsoft"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Definir configurações de política do Microsoft Edge no Windows | Documentos da Microsoft"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
