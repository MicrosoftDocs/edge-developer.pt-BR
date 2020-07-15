---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 70fb6f75594284560cb0d64663fbda47cc7404d6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879342"
---
# interface ICoreWebView2ProcessFailedEventArgs 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

Args de evento para o evento ProcessFailed.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_ProcessFailedKind](#get_processfailedkind) | O tipo de falha de processo ocorrida.

## Parte

#### get_ProcessFailedKind 

O tipo de falha de processo ocorrida.

> público HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND * ProcessFailedKind)

