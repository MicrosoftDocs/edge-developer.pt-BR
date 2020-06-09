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
ms.openlocfilehash: b5fcd04d702483778ef31549c2e7d989ebfe3689
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698291"
---
# interface ICoreWebView2Deferral 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

Essa interface é usada para concluir adiamentos em argumentos de evento que dão suporte a obter adiamentos por meio do método.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[Concluída](#complete) | Conclui o evento adiado associado.

## Parte

#### Concluída 

Conclui o evento adiado associado.

> público HRESULT [concluído](#complete)()

Concluir só deve ser chamado uma vez para cada adiamento tirado.

