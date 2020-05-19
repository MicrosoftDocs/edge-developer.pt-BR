---
description: Saiba como depurar controles WebView2.
title: Depurando WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 386bc237257be0ade8c48bc1c737b0151a882719
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659676"
---
# Como depurar ao desenvolver com controles WebView2  

O objetivo do controle WebView2 do Microsoft Edge é combinar o melhor dos recursos de desenvolvimento de aplicativos Web e nativo e ferramentas de desenvolvedor.  Este artigo descreve as diferentes ferramentas a serem usadas ao desenvolver com controles WebView2.  

## Microsoft Edge DevTools  

Use as [ferramentas de desenvolvedor do Microsoft Edge (Chromium)](/microsoft-edge/devtools-guide-chromium) para depurar o conteúdo da Web exibido em controles WebView2, da mesma forma que faria se estivesse usando o Microsoft Edge.  Para abrir o DevTools, defina o foco na janela do WebView e use qualquer uma das opções a seguir.  
*   Selecione `F12` .  
*   Selecione `Ctrl` + `Shift` + `I` .  
*   Abra o menu de contexto \ (clique com o botão direito do mouse \) > selecionar `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> Quando você depura o aplicativo no Visual Studio com o depurador nativo anexado, a seleção `F12` pode disparar o depurador nativo em vez de ferramentas de desenvolvedor.  Use `Ctrl` + `Shift` + `I` ou use o menu de contexto \ (clique com o botão direito do mouse \) para evitar essa situação.  

## Visual Studio  

Use o depurador de script do Visual Studio 2019 versão 16,4 Preview 2 ou posterior para depurar seu script no Visual Studio.  Verifique se o componente de **diagnóstico JavaScript** em **desenvolvimento de área de trabalho com carga de trabalho C++** está instalado.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnóstico do JavaScript do Visual Studio":::
   Diagnóstico do JavaScript do Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Para habilitar a depuração de script do WebView2, abra o menu de contexto \ (clique com o botão direito do mouse \) em seu projeto > selecione **Propriedades**.  Em **Propriedades de configuração**, selecione **depuração**.  Na propriedade **tipo de depurador** , escolha **JavaScript (WebView2)** na lista de opções. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador do JavaScript do Visual Studio":::
   Depurador do JavaScript do Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## Visual Studio Code  

Você pode usar o código do Visual Studio para depurar scripts executados em controles WebView2.  Para obter mais informações, consulte [aplicativos do Microsoft Edge (Chromium) WebView](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).  

<!--todo:  add See also heading  -->  

## Entrar em contato com a equipe do Microsoft Edge WebView  

Ajude a criar uma experiência de WebView2 mais rica compartilhando seus comentários.  Acesse o [repositório de comentários](https://aka.ms/webviewfeedback) para enviar solicitações de recursos ou relatórios de erros.  
