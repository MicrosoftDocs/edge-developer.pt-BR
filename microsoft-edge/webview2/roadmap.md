---
description: Saiba mais sobre o que está por vir para WebView2
title: Roteiro para o Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicativos win32, win32, edge, ICoreWebView2, ICoreWebView2Host, controle de navegador, html de borda
ms.openlocfilehash: 0f51b5cab32bdb9b9aa9b6baceef5fe5a17eea54
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398410"
---
# <a name="microsoft-edge-webview2-roadmap"></a>Roteiro do Microsoft Edge WebView2  

> [!NOTE]
> Last Updated: November 2020  

O controle WebView2 permite que os desenvolvedores invistam tecnologias web em seus aplicativos nativos.  A página a seguir descreve o roteiro prospectivo para WebView2.  

> [!NOTE]
> O WebView2 está em desenvolvimento ativo e o roteiro continua a evoluir com base nas alterações de mercado e nos comentários dos clientes, portanto, observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.  

Se você tiver preocupações ou dúvidas sobre o Roteiro, forneça seus comentários no [repo de comentários.][GithubMicrosoftedgeWebviewfeedbackMain]  

A equipe webView2 está planejando os seguintes grandes esforços para atualizações futuras.  

:::row:::
   :::column span="1":::
      Instalador do Tempo de Execução do WebView2  
   :::column-end:::
   :::column span="2":::
      *   4º trimestre de 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Versão Não Editável  
   :::column-end:::
   :::column span="2":::
      *   4º trimestre de 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Disponibilidade Geral  
   :::column-end:::
   :::column span="2":::
      *   Win32 C/C++ \(Q4 2020\)  
      *   .NET \(Q4 2020\)  
      *   [WinUI 3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <a name="webview2-runtime-and-installer"></a>WebView2 Runtime e Installer  

[O modelo de distribuição Evergreen][ConceptDistributionEvergreenModel] permite direcionar ou encadear a instalação do Tempo de Execução do WebView2 no computador do usuário.  O Evergreen WebView2 Runtime e o instalador atingiram a Disponibilidade Geral \(GA\).  

## <a name="fixed-version"></a>Versão fixa  

[O modelo de distribuição de versão][ConceptsDistributionFixedVersionModel] fixa permite que você empacote os binários do Microsoft Edge dentro do aplicativo nativo.  A Versão Fixa atingiu Disponibilidade Geral \(GA\).  

## <a name="general-availability"></a>Disponibilidade geral  

### <a name="win32-cc"></a>Win32 C/C++  

O SDK do Win32 C/C++ atingiu GA.  

### <a name="net"></a>.NET  

O SDK .NET atingiu GA. 

### <a name="winui-30"></a>WinUI 3.0  

Você pode acessar WebView2 em seus aplicativos UWP usando [Win UI 3.0][UwpToolkitsWinui3Index], atualmente em alfa.  Para obter mais informações sobre como manter-se atualizado, navegue até Roteiro da Biblioteca da Interface do Usuário [do Windows][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribuição evergreen - Distribuição de aplicativos usando webView2 | Microsoft Docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribuição de versão fixa - Distribuição de aplicativos usando webView2 | Microsoft Docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI Library 3.0 Preview 1 (maio de 2020) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentários do WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Roteiro da Biblioteca da Interface do Usuário do Windows - microsoft/microsoft-ui-xaml | GitHub"  
