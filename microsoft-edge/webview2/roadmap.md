---
description: Saiba mais sobre o que está por vir para WebView2
title: Roteiro para Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 7b67e4a6844ead0f845667a70df8657745ece938
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643417"
---
# <a name="microsoft-edge-webview2-roadmap"></a>Microsoft Edge Roteiro webView2  

> [!NOTE]
> Last Updated: July 2021  

O controle WebView2 permite que os desenvolvedores invistam tecnologias web em seus aplicativos nativos.  A página a seguir descreve o roteiro prospectivo para WebView2.  

> [!NOTE]
> O WebView2 está em desenvolvimento ativo e o roteiro continua a evoluir com base nas alterações de mercado e nos comentários dos clientes, portanto, observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.  

Se você tiver preocupações ou dúvidas sobre o Roteiro, forneça seus comentários no [repo de comentários.][GithubMicrosoftedgeWebviewfeedbackMain]  

A equipe webView2 está planejando os seguintes grandes esforços para atualizações futuras.  

* Visualização UWP
* Visualização do MacOS
* Visualização do Xbox
* HoloLens Visualizar

## <a name="webview2-runtime-and-installer"></a>WebView2 Runtime e Installer  

[O modelo de distribuição Evergreen][ConceptDistributionEvergreenModel] permite direcionar ou encadear a instalação do Tempo de Execução do WebView2 no computador do usuário.  O Evergreen WebView2 Runtime e o instalador atingiram a Disponibilidade Geral \(GA\).  

## <a name="fixed-version"></a>Versão fixa  

[O modelo de distribuição de versão][ConceptsDistributionFixedVersionModel] fixa permite que você empacote os Microsoft Edge binários dentro do aplicativo nativo.  A Versão Fixa atingiu Disponibilidade Geral \(GA\).  

## <a name="general-availability"></a>Disponibilidade geral  

### <a name="win32-cc"></a>Win32 C/C++  

O SDK do Win32 C/C++ atingiu GA.  

### <a name="net"></a>.NET  

O SDK .NET atingiu GA. 

### <a name="windows-ui-library-3"></a>Windows Biblioteca de interface do usuário 3

Você pode acessar controles WebView2 em seus aplicativos usando Windows biblioteca de interface do usuário [3 (WinUI3)][UwpToolkitsWinui3Index] com o SDK do Windows App. Isso está atualmente em visualização. Para obter mais informações, navegue até o [mapa Windows SDK do aplicativo.][WindowsAppSDK|::ref1::|]

 
<!-- links -->  

[WindowsAppSDKRoadmap]: https://github.com/microsoft/WindowsAppSDK/blob/main/docs/roadmap.md "Roteiro"
[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribuição evergreen - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribuição de versão fixa - Distribuição de aplicativos usando webView2 | Microsoft Docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows Biblioteca de interface do usuário 3.0 Visualização 1 (maio de 2020) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Roteiro da Biblioteca da Interface do Usuário - microsoft/microsoft-ui-xaml | GitHub"  
