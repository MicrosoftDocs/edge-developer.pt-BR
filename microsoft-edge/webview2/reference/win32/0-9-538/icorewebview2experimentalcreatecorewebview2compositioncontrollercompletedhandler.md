---
description: Inserir tecnologias da Web (HTML, CSS e JavaScript) em seus aplicativos nativos com o controle WebView2 do Microsoft Edge
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, controle do navegador, HTML Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: 8fc3efa6bf1ba9a9e721dcba67e8350ded38cc62
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011130"
---
# 0.9.579-ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler de interface 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

> [chamada](#invoke)a Public HRESULT (resultado HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * WebView)

