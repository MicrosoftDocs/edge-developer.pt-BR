---
description: Modelo de threading
title: Modelo de threading
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013734"
---
# Modelo de threading 

O controle WebView2 é baseado no [modelo de objeto componente (com)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) e deve ser executado em um [único thread de Apartments (STA) segmentado](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) .

## Segurança de thread  

O WebView2 deve ser criado em um thread de interface do usuário.  Especificamente um thread com um bombeamento de mensagem.  Todos os retornos de chamada ocorrem nesse thread e as solicitações no WebView2 devem ser feitas nesse thread.  Não é seguro usar o WebView2 de outro thread.  

A única exceção é para a `Content` propriedade `CoreWebView2WebResourceRequest` .  O `Content` fluxo de propriedades é lido a partir de um thread em segundo plano.  O fluxo deve ser ágil ou ser criado a partir de um STA em segundo plano para evitar o impacto de desempenho no thread da interface do usuário.  

## Reentrância  

Os retornos de chamada, incluindo manipuladores de eventos e manipuladores de conclusão, são executados em série.  Se você tiver um manipulador de eventos em execução e iniciar um loop de mensagem, nenhum outro manipulador de eventos ou retornos de chamada de conclusão poderão começar a ser executados de forma reentrante.  

## Adiamentos  

Alguns eventos WebView2 lêem valores definidos em seus argumentos de evento ou executam alguma ação após a conclusão do manipulador de eventos.  Se você também precisar executar uma operação assíncrona, como um manipulador de eventos, você pode usar o `GetDeferral` método nos argumentos do evento dos eventos associados.  O objeto de adiamento retornado garante que o manipulador de eventos não seja considerado concluído até que o `Complete` método de `Deferral` seja solicitado.  

Por exemplo, você pode usar o `NewWindowRequested` evento para fornecer uma `CoreWebView2` janela para conectar-se como uma janela filho quando o manipulador de eventos é concluído.  Mas se você precisar criar assincronamente o `CoreWebView2` , solicite o `GetDeferral` método no `NewWindowRequestedEventArgs` .  Depois que você tiver criado assincronamente a `CoreWebView2` e definir a `NewWindow` propriedade no `NewWindowRequestedEventArgs` objeto, a solicitação `Complete` no `Deferral` objeto será retornada usando o `GetDeferral` método.  

<!-- links -->  
