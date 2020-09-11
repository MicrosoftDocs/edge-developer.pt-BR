---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, app, Edge, CoreWebView2, CoreWebView2Controller, controle do navegador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: c7f318f44ce0469a216fe8dda7870c4adbdebcc0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011505"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs 

Namespace: Microsoft. Web. WebView2. Core \
Assembly: Microsoft.Web.WebView2.Core.dll

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

