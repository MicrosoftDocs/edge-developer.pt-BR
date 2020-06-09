---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: de0319060b6e618c30fc685815bcbcc41e8c3005
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697844"
---
# interface ICoreWebView2MoveFocusRequestedEventArgs 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento MoveFocusRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Handled](#get_handled) | Indique se o evento foi manipulado pelo aplicativo.
[get_Reason](#get_reason) | O motivo do WebView disparar o evento MoveFocus solicitado.
[put_Handled](#put_handled) | Defina a propriedade Handled.

## Parte

#### get_Handled 

Indique se o evento foi manipulado pelo aplicativo.

> [get_Handled](#get_handled)público HRESULT (valor bool *)

Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE. Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada. A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela. Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.

#### get_Reason 

O motivo do WebView disparar o evento MoveFocus solicitado.

> [get_Reason](#get_reason)público HRESULT (COREWEBVIEW2_MOVE_FOCUS_REASON * valor)

#### put_Handled 

Defina a propriedade Handled.

> [put_Handled](#put_handled)público HRESULT (valor bool)

