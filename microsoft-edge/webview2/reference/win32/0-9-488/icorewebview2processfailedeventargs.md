---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 0efc1656b8204b9775002db49e0e4a5734682cc4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652361"
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

