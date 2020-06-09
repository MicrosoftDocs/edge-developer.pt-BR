---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: b44bd47f5352179abcc06ef5fd5b8f613bde455e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698278"
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

