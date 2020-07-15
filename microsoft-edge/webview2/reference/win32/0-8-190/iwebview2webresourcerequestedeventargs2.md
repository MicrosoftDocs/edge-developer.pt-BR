---
description: Hospedar conteúdo da Web em seu aplicativo Win32 com o controle WebView2 do Microsoft Edge
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicativos Win32, Win32, Edge
ms.openlocfilehash: 80ea596f28d1afeb451ce20d495961ca4eed507a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878110"
---
# 0.8.355-IWebView2WebResourceRequestedEventArgs2 de interface 

> [!NOTE]
> Essa interface pode ser alterada ou indisponível para versões posteriores SDK da versão 0.8.355. Consulte a [referência](../../../webview2-api-reference.md) para obter a referência da API mais recente.

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

Args de evento para o evento WebResourceRequested.

## Resumo

 Parte                        | Descrições
--------------------------------|---------------------------------------------
[get_ResourceContext](#get_resourcecontext) | Os contextos de solicitação de recurso da Web.

## Parte

#### get_ResourceContext 

Os contextos de solicitação de recurso da Web.

> [get_ResourceContext](#get_resourcecontext)público HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT * contexto)

