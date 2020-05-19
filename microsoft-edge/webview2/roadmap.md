---
description: Saiba mais sobre o que vem a seguir para WebView2
title: Mapa da WebView da Microsoft Edge 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: bc55c5a731ab6cba8f9be15208029aad0ad5357a
ms.sourcegitcommit: a75e062b71831ea850c85287a8d7d7ce3b55ec84
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659741"
---
# Mapa de WebView2 do Microsoft Edge

##### Última atualização: maio de 2020

O controle WebView2 permite que os desenvolvedores insiram tecnologias da Web em seus aplicativos nativos. Este documento descreve o roteiro potencial para WebView2. 

> [!NOTE]
> O WebView2 está em desenvolvimento ativo, e o roteiro continuará evoluindo com base nas mudanças do mercado e nos comentários dos clientes, portanto observe que os planos descritos aqui não são exaustivos e estão sujeitos a alterações. 

Se você tiver dúvidas ou dúvidas sobre o roteiro, deixe comentários no repositório de [comentários](https://github.com/MicrosoftEdge/WebViewFeedback).

A equipe WebView2 tem alguns esforços importantes em andamento:

1.  Instalador do WebView2 Runtime (Q4 2020)
2.  Versão corrigida (Q4 2020)
3.  Disponibilidade geral 
    *   Win32 C/C++ (4º trimestre de 2020)
    *   .NET (Q4 2020)
    *   [WinUI 3,0](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## Instalador & do WebView2 Runtime

WebView2 o modelo de distribuição [verde](./concepts/distribution.md#microsoft-edge-webview2-runtime) permitirá que você direcione ou reinstale o tempo de execução do WebView2 na máquina do usuário. Espera-se que uma visualização do tempo de execução do WebView2 e do instalador esteja disponível no 3º trimestre de 2020 e em GA 2020.

## Versão corrigida

O modelo de distribuição [fixa](./concepts/distribution.md#roadmap) WebView2 permite empacotar os binários do Microsoft Edge dentro de seu aplicativo nativo. No momento, o trabalho de engenharia está em meio a uma visualização prevista para estar pronto até o final do 3º trimestre de 2020 e do GA trimestre de 2020.

## Disponibilidade geral 

### Win32 C/C++

O SDK do Win32 C/C++ é esperado para GA no quarto trimestre de 2020, logo depois do tempo de execução do WebView2 e do instalador GA.

### .NET

O SDK do .NET encapsula o SDK C/C++ do Win32. O SDK do .NET é esperado para GA, logo após o Win32 C/C++ GA no quarto trimestre de 2020.

### WinUI 3,0

Você pode trazer o WebView2 para aplicativos UWP por meio [da interface do usuário do Win 3,0](/uwp/toolkits/winui3/), atualmente em Alpha. Fazer check-out do [roteiro da Windows UI library](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) para manter-se atualizado.  
