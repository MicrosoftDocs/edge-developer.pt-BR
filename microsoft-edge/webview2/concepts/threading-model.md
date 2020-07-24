---
description: Modelo de Threading
title: Modelo de Threading
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: ad51afee97d3cc3e913ecdd73c4f0c2a99c70564
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895530"
---
# Modelo de Threading  

## Segurança de thread  

O WebView2 deve ser criado em um thread de interface do usuário.  Especificamente um thread com um bombeamento de mensagem.  Todos os retornos de chamada ocorrem nesse thread e as solicitações no WebView2 devem ser feitas nesse thread.  Não é seguro usar o WebView2 de outro thread.  

A única exceção é para a `Content` propriedade `CoreWebView2WebResourceRequest` .  O `Content` fluxo de propriedades é lido a partir de um thread em segundo plano.  O fluxo deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto de desempenho no thread da interface do usuário.  

## Reentrância  

Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série.  Se você tiver um manipulador de eventos em execução e iniciar um loop de mensagem, nenhum outro manipulador de eventos ou retornos de chamada de conclusão poderão começar a ser executados de forma reentrante.  

## Adiamentos  

Alguns eventos WebView2 lêem valores definidos em seus argumentos de evento ou executam alguma ação após a conclusão do manipulador de eventos.  Se você também precisar executar uma operação assíncrona, como um manipulador de eventos, você pode usar o `GetDeferral` método nos argumentos do evento dos eventos associados.  O objeto de adiamento retornado garante que o manipulador de eventos não seja considerado concluído até que o `Complete` método de `Deferral` seja solicitado.  

Por exemplo, você pode usar o `NewWindowRequested` evento para fornecer uma `CoreWebView2` janela para conectar-se como uma janela filho quando o manipulador de eventos é concluído.  Mas se você precisar criar assincronamente o `CoreWebView2` , solicite o `GetDeferral` método no `NewWindowRequestedEventArgs` .  Depois que você tiver criado assincronamente a `CoreWebView2` e definir a `NewWindow` propriedade no `NewWindowRequestedEventArgs` objeto, a solicitação `Complete` no `Deferral` objeto será retornada usando o `GetDeferral` método.  

<!-- links -->  
