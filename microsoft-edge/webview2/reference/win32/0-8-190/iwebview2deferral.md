---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: f40d0baa415ccc76747993c4070bb05eaf76fe56
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878607"
---
# 0.8.355-IWebView2Deferral de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2Deferral
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

