---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 74cd0451e111780078714b17e5bd1097c56d6b2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877571"
---
# interface ICoreWebView2ZoomFactorChangedEventHandler 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

O chamador implementa essa interface para receber eventos ZoomFactorChanged.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

Use a propriedade ICoreWebView2Controller. ZoomFactor para obter o fator de zoom modificado.

## Parte

#### Invocar 

Chamado para fornecer o implementador com os argumentos do evento para o evento correspondente.

> [chamada](#invoke)a Public HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) * Sender, IUnknown * args)

Não há argumentos de evento e o parâmetro args será nulo.

