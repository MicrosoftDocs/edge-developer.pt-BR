---
description: Saiba mais sobre o que vem a seguir para WebView2
title: Mapa da WebView da Microsoft Edge 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 99e743db0c1fb17ea46405b08e1ed074a3386068
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182357"
---
# Mapa de WebView2 do Microsoft Edge  

##### Última atualização: novembro de 2020  

O controle WebView2 permite que os desenvolvedores insiram tecnologias da Web em seus aplicativos nativos.  A página a seguir descreve o mapa potencial para WebView2.  

> [!NOTE]
> O WebView2 está em desenvolvimento ativo, e o mapa continua a evoluir com base nas mudanças do mercado e nos comentários dos clientes, portanto, observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações.  

Se você tiver dúvidas ou dúvidas sobre o roteiro, forneça seus comentários no [repositório de comentários][GithubMicrosoftedgeWebviewfeedbackMain].  

A equipe do WebView2 está planejando os principais esforços para atualizações futuras.  

:::row:::
   :::column span="1":::
      Instalador do WebView2 Runtime  
   :::column-end:::
   :::column span="2":::
      *   Quarto trimestre de 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Versão Não Editável  
   :::column-end:::
   :::column span="2":::
      *   Quarto trimestre de 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Disponibilidade geral  
   :::column-end:::
   :::column span="2":::
      *   Win32 C/C++ \ (Q4 2020 \)  
      *   .NET \ (Q4 2020 \)  
      *   [WinUI 3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## Tempo de execução do WebView2 e instalador  

O [modelo de distribuição verde][ConceptDistributionEvergreenModel] permite que você direcione ou reinstale o tempo de execução do WebView2 no computador do usuário.  O tempo de execução do WebView2 e o instalador do verde chegaram à disponibilidade geral \ (GA \).  

## Versão corrigida  

O [modelo de distribuição de versão fixa][ConceptsDistributionFixedVersionModel] permite empacotar os binários do Microsoft Edge dentro de seu aplicativo nativo.  A versão corrigida atingiu a disponibilidade geral \ (GA \).  

## Disponibilidade geral  

### Win32 C/C++  

O SDK C/C++ do Win32 alcançou GA.  

### .NET  

O SDK do .NET alcançou o GA. 

### WinUI 3.0  

Você pode acessar o WebView2 em seus aplicativos UWP usando a [interface do usuário do Win 3,0][UwpToolkitsWinui3Index], atualmente em Alpha.  Para obter mais informações sobre como manter-se atualizado, consulte o [mapa de biblioteca da interface do usuário do Windows][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribuição verde-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribuição de versão fixa-distribuição de aplicativos usando o WebView2 | Documentos da Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows UI library 3,0 Preview 1 (2020 de maio) | Documentos da Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Feedback da WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Mapa da Windows UI library-Microsoft/Microsoft-UI-XAML | GitHub"  
