---
description: Modelo de processo
title: Modelo de processo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895531"
---
# Modelo de processo  

O WebView2 usa o mesmo modelo de processo do navegador Microsoft Edge.  Para obter mais informações sobre o modelo de processo do navegador, consulte [arquitetura do navegador – examine o navegador da Web moderno][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]. 

Um processo do navegador está associado aos processos do renderizador e outros processos do utilitário conforme descrito nesse artigo.  Além disso, no caso do WebView2, há um aplicativo host solicitando processos usando WebView2.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Processo 1" lightbox="../media/process-model-1.png":::
   Processo 1  
:::image-end:::  

Um processo do navegador é especificado na pasta dados do usuário em uma sessão do usuário que atende a qualquer WebView2 que solicita o processo que especifica a pasta dados do usuário.  Isso significa que um processo de navegador pode estar servindo vários processos de solicitação e um processo de solicitação pode estar usando vários processos do navegador.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Processo 2" lightbox="../media/process-model-2.png":::
   Processo 2  
:::image-end:::  

Um processo de navegador tem alguns processos de renderização associados.  Os processos do navegador são criados conforme necessário para atender a potencialmente vários quadros em diferentes instâncias do WebView2.  O número de processos de renderização varia de acordo com o recurso de navegador de isolamento de site e o número de origens discadas discadas renderizadas em instâncias associadas do WebView2.  O recurso de navegador de isolamento de site é descrito no conteúdo anterior.  

O `CoreWebView2Environment` representa um processo de navegador e pasta de dados do usuário.  O `CoreWebView2` não corresponde diretamente a qualquer conjunto de processos, pois vários processos de renderização são usados por um WebView2 dependendo do isolamento do site conforme descrito anteriormente.  

Você pode reagir a falhas e travamentos nesses processos de navegador e renderização usando o `ProcessFailed` evento de `CoreWebView2` .  

Você pode desligar com segurança os processos do navegador e do renderizador associados usando o `Close` método of `CoreWebView2Controller` .  

Para abrir a janela do Gerenciador de tarefas do navegador da janela do **devtools** de uma instância do WebView2, você pode selecionar `Shift` + `Escape` ou passar o mouse na barra de título da janela do devtools, abrir o menu contextual \(clique com o botão direito do mouse \) e escolher `Browser task manager` .  Todos os processos associados ao processo do navegador de seu WebView2 são exibidos incluindo finalidades associadas.  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitetura do navegador – veja dentro do navegador da Web moderno (parte 1)"  
