---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 69835f6fe22246f43e3df9c45a7fde7a674ac0e5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697641"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Args de evento para o evento MoveFocusRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Handled](#handled) | Indique se o evento foi manipulado pelo aplicativo.
[Motivo](#reason) | O motivo do WebView disparar o evento MoveFocus solicitado.

## Parte

#### Handled 

Indique se o evento foi manipulado pelo aplicativo.

> bool público [manipulado](#handled)

Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE. Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada. A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela. Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.

#### Motivo 

O motivo do WebView disparar o evento MoveFocus solicitado.

> [motivo](#reason) CoreWebView2MoveFocusReason público

