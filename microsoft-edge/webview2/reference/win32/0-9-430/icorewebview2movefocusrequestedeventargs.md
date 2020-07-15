---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, controle do navegador, HTML Edge
ms.openlocfilehash: fe0c0fae0ec33cbc5ba50ca163b3f4fc8baa61b9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880952"
---
# 0.9.430-ICoreWebView2MoveFocusRequestedEventArgs de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.430. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

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

