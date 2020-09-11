---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 96fff3ab67331bf5a8cf8323af5dddbca04f9e0e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010562"
---
# 0.9.579-ICoreWebView2CapturePreviewCompletedHandler de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

O chamador implementa esse método para receber o resultado do método CapturePreview.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Invocar](#invoke) | Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.

O resultado é gravado no fluxo fornecido na chamada do método CapturePreview.

## Parte

#### Invocar 

Chamado para fornecer o implementador com o status de conclusão da chamada de método assíncrono correspondente.

> [chamada](#invoke)a Public HRESULT (resultado HRESULT)

