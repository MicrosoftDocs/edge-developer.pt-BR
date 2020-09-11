---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: fd762c994d4c42e5e92dec09add2aa3b85b0ec80
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011487"
---
# interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2CompositionController.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.

> [chamada](#invoke)a Public HRESULT (HRESULT ErrorCode, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * WebView)

