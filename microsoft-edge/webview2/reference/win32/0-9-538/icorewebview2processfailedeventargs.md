---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: af27c39b2ed9ba197ab1c567bcf18a43c3dee932
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010016"
---
# 0.9.579-ICoreWebView2ProcessFailedEventArgs de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

