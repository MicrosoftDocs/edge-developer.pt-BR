---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: f58279d1a3c404715be5aad8bf1be5ef120e1d94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880000"
---
# interface ICoreWebView2ExperimentalCursorChangedEventHandler 

> [!NOTE]
> Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber eventos CursorChanged.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

Use a propriedade cursor para obter o novo cursor.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> [chamada](#invoke)a Public HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * Sender, IUnknown * args)

Não há argumentos de evento e o parâmetro args será nulo.

