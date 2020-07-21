---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: 643e2e998cc8ca70bfd90fbcb9bbf1f6c690322b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884544"
---
# 0.9.430-ICoreWebView2MoveFocusRequestedEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventArgs
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

> [get_Reason](#get_reason)público HRESULT (CORE_WEBVIEW2_MOVE_FOCUS_REASON * valor)

#### get_Handled 

Indique se o evento foi manipulado pelo aplicativo.

> [get_Handled](#get_handled)público HRESULT (valor bool *)

Se o aplicativo tiver movido o foco para o local desejado, ele deve definir a propriedade Handled como TRUE. Quando a propriedade Handled é falsa após o manipulador de eventos retornar, a ação padrão será tomada. A ação padrão é tentar encontrar a próxima janela de término da parada de tabulação no aplicativo e tentar mover o foco para essa janela. Se não houver outra janela para a qual mover o foco, o foco será perfocado dentro do conteúdo da Web da WebView.

#### put_Handled 

Defina a propriedade Handled.

> [put_Handled](#put_handled)público HRESULT (valor bool)

