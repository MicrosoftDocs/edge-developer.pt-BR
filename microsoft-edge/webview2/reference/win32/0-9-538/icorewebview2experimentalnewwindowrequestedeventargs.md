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
ms.openlocfilehash: 1d91bb767045179a5d8de3700f86ff6d92a9ef36
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698399"
---
# interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs 

> [!NOTE]
> Esta é uma API experimental que é fornecida com a versão 0.9.538 do SDK de pré-lançamento.

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

Args de evento para o evento NewWindowRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_WindowFeatures](#get_windowfeatures) | Recursos de janela especificados pela chamada Window. Open.

O evento é acionado quando o conteúdo da WebView é solicitado para abrir uma nova janela (por meio de Window. Open () e assim por diante.)

## Parte

#### get_WindowFeatures 

Recursos de janela especificados pela chamada Window. Open.

> Public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) * * WindowFeatures)

Esses recursos podem ser considerados para o posicionamento e o dimensionamento de novas janelas da WebView.

