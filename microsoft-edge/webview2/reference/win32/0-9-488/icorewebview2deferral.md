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
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10652622"
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

