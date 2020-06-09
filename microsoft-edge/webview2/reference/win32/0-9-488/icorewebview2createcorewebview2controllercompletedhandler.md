---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: Microsoft Edge WebView2 para aplicativos Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge
ms.openlocfilehash: 0fb633a45df15c5b5116d69f74f6d12894bc91c1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698089"
---
# interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler 

> [!NOTE]
> Esta referência pode ser alterada ou indisponível para versões posteriores SDK da versão 0.9.515. Consulte a [referência de API WebView2](../../../webview2-api-reference.md) para obter a referência de API mais recente.

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

O chamador implementa essa interface para receber a CoreWebView2Controller criada via CreateCoreWebView2Controller.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.

## Parte

#### Invocar 

Chamado para fornecer o implementador com o status de conclusão e o resultado da chamada de método assíncrono correspondente.

> [chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) * createdController)

