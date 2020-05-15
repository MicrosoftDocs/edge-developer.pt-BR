---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 2e3afec26b0e09a80182118f74b6f50733b0c71a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652539"
---
# interface IWebView2MoveFocusRequestedEventArgs 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento MoveFocusRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_Reason](#get_reason) | O motivo do WebView disparar o evento MoveFocus solicitado.
[get_Handled](#get_handled) | Indique se o evento foi manipulado pelo aplicativo.
[put_Handled](#put_handled) | Defina a propriedade Handled.

## Parte

#### get_Reason 

O motivo do WebView disparar o evento MoveFocus solicitado.

> [get_Reason](#get_reason)público HRESULT (WEBVIEW2_MOVE_FOCUS_REASON * valor)

#### get_Handled 

Indique se o evento foi manipulado pelo aplicativo.

> [get_Handled](#get_handled)público HRESULT (valor bool *)

Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE. Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada. A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela. Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.

#### put_Handled 

Defina a propriedade Handled.

> [put_Handled](#put_handled)público HRESULT (valor bool)

